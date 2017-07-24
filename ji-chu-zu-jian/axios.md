Api请求，除了可以使用fetch外，同样可以使用axios组件

在使用axios发送x-www-form-urlencoded请求时，需要使用qs组件

```
import axios from 'axios';
import qs from 'qs';

const func = (email, password) => {
	const data = qs.stringify({ email, password });
	return axios.post(url, data).catch(e => {
		return Promise.resolve({ data: { code: 1, msg: '请求错误' } })
	}).then(res => res.data);
};
```



