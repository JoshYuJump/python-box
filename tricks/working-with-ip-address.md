## 002 获取ip地址的类型

---

```python
# 你可以获取到某个对象的字符串格式的类名:

>>> import ipaddress
 
# 判断IP地址类型
>>> ipaddress.ip_address('192.168.1.2')
IPv4Address('192.168.1.2')

>>> ipaddress.ip_address('2001:af3::')
IPv6Address('2001:af3::')
 
# 获取ipaddress 所有属性集合
>>> dir(ipaddress)
>>>['AddressValueError', 'IPV4LENGTH', 'IPV6LENGTH', 'IPv4Address', 'IPv4Interface', 'IPv4Network', 'IPv6Address', 'IPv6Interface', 'IPv6Network', 'NetmaskValueError', '_BaseAddress', '_BaseNetwork', '_BaseV4', '_BaseV6', '_IPAddressBase', '_IPv4Constants', '_IPv6Constants', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '__version__', '_collapse_addresses_internal', '_count_righthand_zero_bits', '_find_address_range', '_split_optional_netmask', 'collapse_addresses', 'functools', 'get_mixed_type_key', 'ip_address', 'ip_interface', 'ip_network', 'summarize_address_range', 'v4_int_to_packed', 'v6_int_to_packed']

```

> 原文：https://docs.python.org/3/library/ipaddress.html
