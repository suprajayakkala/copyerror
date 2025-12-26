# copyerror

PS C:\Users\susaisup\Downloads\fastapi-log-main> .\.venv\Scripts\Activate.ps1
(.venv) PS C:\Users\susaisup\Downloads\fastapi-log-main> python -m uvicorn main:app --reload --host 127.0.0.1 --port 80   
>>      
INFO:     Will watch for changes in these directories: ['C:\\Users\\susaisup\\Downloads\\fastapi-log-main']
INFO:     Uvicorn running on http://127.0.0.1:80 (Press CTRL+C to quit)
INFO:     Started reloader process [1064] using WatchFiles
2025-12-26 21:43:09,404 INFO sqlalchemy.engine.Engine SELECT DATABASE()
INFO:sqlalchemy.engine.Engine:SELECT DATABASE()
2025-12-26 21:43:09,405 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,407 INFO sqlalchemy.engine.Engine SELECT @@sql_mode
INFO:sqlalchemy.engine.Engine:SELECT @@sql_mode
2025-12-26 21:43:09,407 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,408 INFO sqlalchemy.engine.Engine SELECT @@lower_case_table_names
INFO:sqlalchemy.engine.Engine:SELECT @@lower_case_table_names
2025-12-26 21:43:09,408 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,410 INFO sqlalchemy.engine.Engine BEGIN (implicit)
INFO:sqlalchemy.engine.Engine:BEGIN (implicit)
2025-12-26 21:43:09,410 INFO sqlalchemy.engine.Engine DESCRIBE `shopping_cart`.`user_tbl`
INFO:sqlalchemy.engine.Engine:DESCRIBE `shopping_cart`.`user_tbl`
2025-12-26 21:43:09,410 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,432 INFO sqlalchemy.engine.Engine DESCRIBE `shopping_cart`.`categories`
INFO:sqlalchemy.engine.Engine:DESCRIBE `shopping_cart`.`categories`
2025-12-26 21:43:09,433 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,436 INFO sqlalchemy.engine.Engine DESCRIBE `shopping_cart`.`products`
INFO:sqlalchemy.engine.Engine:DESCRIBE `shopping_cart`.`products`
2025-12-26 21:43:09,436 INFO sqlalchemy.engine.Engine [raw sql] {}
INFO:sqlalchemy.engine.Engine:[raw sql] {}
2025-12-26 21:43:09,439 INFO sqlalchemy.engine.Engine COMMIT
INFO:sqlalchemy.engine.Engine:COMMIT
INFO:     Started server process [20200]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     127.0.0.1:64739 - "GET / HTTP/1.1" 404 Not Found
INFO:     127.0.0.1:52680 - "GET /docd HTTP/1.1" 404 Not Found
INFO:     127.0.0.1:52680 - "GET /docs HTTP/1.1" 200 OK
INFO:     127.0.0.1:52680 - "GET /openapi.json HTTP/1.1" 200 OK
INFO:database:📦 DB session opened
INFO:products:📦 Fetching products
2025-12-26 21:43:29,429 INFO sqlalchemy.engine.Engine BEGIN (implicit)
INFO:sqlalchemy.engine.Engine:BEGIN (implicit)
2025-12-26 21:43:29,432 INFO sqlalchemy.engine.Engine SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products
INFO:sqlalchemy.engine.Engine:SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products
2025-12-26 21:43:29,433 INFO sqlalchemy.engine.Engine [generated in 0.00058s] {}
INFO:sqlalchemy.engine.Engine:[generated in 0.00058s] {}
2025-12-26 21:43:29,446 INFO sqlalchemy.engine.Engine ROLLBACK
INFO:sqlalchemy.engine.Engine:ROLLBACK
INFO:database:📦 DB session closed
INFO:     127.0.0.1:50060 - "GET /products/ HTTP/1.1" 500 Internal Server Error
ERROR:    Exception in ASGI application
Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1967, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\default.py", line 952, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 153, in execute    
    result = self._query(query)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 322, in _query     
    conn.query(q)
    ~~~~~~~~~~^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 575, in query  
    self._affected_rows = self._read_query_result(unbuffered=unbuffered)
                          ~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 826, in _read_query_result
    result.read()
    ~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 1203, in read  
    first_packet = self.connection._read_packet()
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 782, in _read_packet
    packet.raise_for_error()
    ~~~~~~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\protocol.py", line 219, in raise_for_error
    err.raise_mysql_exception(self._data)
    ~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\err.py", line 150, in raise_mysql_exception
    raise errorclass(errno, errval)
pymysql.err.OperationalError: (1054, "Unknown column 'products.product_name' in 'field list'")

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\protocols\http\httptools_impl.py", line 416, in run_asgi
    result = await app(  # type: ignore[func-returns-value]
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        self.scope, self.receive, self.send
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\middleware\proxy_headers.py", line 60, in __call__
    return await self.app(scope, receive, send)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\applications.py", line 1135, in __call__
    await super().__call__(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\applications.py", line 107, in __call__
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 186, in __call__
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 164, in __call__
    await self.app(scope, receive, _send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\exceptions.py", line 63, in __call__
    await wrap_app_handling_exceptions(self.app, conn)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\middleware\asyncexitstack.py", line 18, in __call__
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 716, in __call__ 
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 736, in app      
    await route.handle(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 290, in handle   
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 119, in app        
    await wrap_app_handling_exceptions(app, request)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 105, in app        
    response = await f(request)
               ^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 426, in app        
    raw_response = await run_endpoint_function(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    ...<3 lines>...
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 314, in run_endpoint_function
    return await run_in_threadpool(dependant.call, **values)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\concurrency.py", line 32, in run_in_threadpool
    return await anyio.to_thread.run_sync(func)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\to_thread.py", line 61, in run_sync    
    return await get_async_backend().run_sync_in_worker_thread(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        func, args, abandon_on_cancel=abandon_on_cancel, limiter=limiter
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 2525, in run_sync_in_worker_thread
    return await future
           ^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 986, in run
    result = context.run(func, *args)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\products.py", line 25, in list_products
    return query.all()
           ~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\query.py", line 2704, in all  
    return self._iter().all()  # type: ignore
           ~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\query.py", line 2857, in _iter
    result: Union[ScalarResult[_T], Result[_T]] = self.session.execute(
                                                  ~~~~~~~~~~~~~~~~~~~~^
        statement,
        ^^^^^^^^^^
        params,
        ^^^^^^^
        execution_options={"_sa_orm_load_options": self.load_options},
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\session.py", line 2351, in execute
    return self._execute_internal(
           ~~~~~~~~~~~~~~~~~~~~~~^
        statement,
        ^^^^^^^^^^
    ...<4 lines>...
        _add_event=_add_event,
        ^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\session.py", line 2249, in _execute_internal
    result: Result[Any] = compile_state_cls.orm_execute_statement(
                          ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self,
        ^^^^^
    ...<4 lines>...
        conn,
        ^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\context.py", line 306, in orm_execute_statement
    result = conn.execute(
        statement, params or {}, execution_options=execution_options
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1419, in execute
    return meth(
        self,
        distilled_parameters,
        execution_options or NO_OPTIONS,
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\sql\elements.py", line 527, in _execute_on_connection
    return connection._execute_clauseelement(
           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self, distilled_params, execution_options
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1641, in _execute_clauseelement
    ret = self._execute_context(
        dialect,
    ...<8 lines>...
        cache_hit=cache_hit,
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1846, in _execute_context
    return self._exec_single_context(
           ~~~~~~~~~~~~~~~~~~~~~~~~~^
        dialect, context, statement, parameters
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1986, in _exec_single_context
    self._handle_dbapi_exception(
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        e, str_statement, effective_parameters, cursor, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 2363, in _handle_dbapi_exception
    raise sqlalchemy_exception.with_traceback(exc_info[2]) from e
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1967, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\default.py", line 952, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 153, in execute    
    result = self._query(query)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 322, in _query     
    conn.query(q)
    ~~~~~~~~~~^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 575, in query  
    self._affected_rows = self._read_query_result(unbuffered=unbuffered)
                          ~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 826, in _read_query_result
    result.read()
    ~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 1203, in read  
    first_packet = self.connection._read_packet()
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 782, in _read_packet
    packet.raise_for_error()
    ~~~~~~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\protocol.py", line 219, in raise_for_error
    err.raise_mysql_exception(self._data)
    ~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\err.py", line 150, in raise_mysql_exception
    raise errorclass(errno, errval)
sqlalchemy.exc.OperationalError: (pymysql.err.OperationalError) (1054, "Unknown column 'products.product_name' in 'field list'")
[SQL: SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products]
(Background on this error at: https://sqlalche.me/e/20/e3q8)
INFO:database:📦 DB session opened
INFO:products:📦 Fetching products
2025-12-26 21:43:36,510 INFO sqlalchemy.engine.Engine BEGIN (implicit)
INFO:sqlalchemy.engine.Engine:BEGIN (implicit)
2025-12-26 21:43:36,513 INFO sqlalchemy.engine.Engine SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products
WHERE products.category_id = %(category_id_1)s AND lower(products.product_name) LIKE lower(%(product_name_1)s)
INFO:sqlalchemy.engine.Engine:SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products
WHERE products.category_id = %(category_id_1)s AND lower(products.product_name) LIKE lower(%(product_name_1)s)
2025-12-26 21:43:36,514 INFO sqlalchemy.engine.Engine [generated in 0.00082s] {'category_id_1': 1, 'product_name_1': '%q%'}
INFO:sqlalchemy.engine.Engine:[generated in 0.00082s] {'category_id_1': 1, 'product_name_1': '%q%'}
2025-12-26 21:43:36,528 INFO sqlalchemy.engine.Engine ROLLBACK
INFO:sqlalchemy.engine.Engine:ROLLBACK
INFO:database:📦 DB session closed
INFO:     127.0.0.1:61847 - "GET /products/?category_id=1&q=q HTTP/1.1" 500 Internal Server Error
ERROR:    Exception in ASGI application
Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1967, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\default.py", line 952, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 153, in execute    
    result = self._query(query)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 322, in _query     
    conn.query(q)
    ~~~~~~~~~~^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 575, in query  
    self._affected_rows = self._read_query_result(unbuffered=unbuffered)
                          ~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 826, in _read_query_result
    result.read()
    ~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 1203, in read  
    first_packet = self.connection._read_packet()
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 782, in _read_packet
    packet.raise_for_error()
    ~~~~~~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\protocol.py", line 219, in raise_for_error
    err.raise_mysql_exception(self._data)
    ~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\err.py", line 150, in raise_mysql_exception
    raise errorclass(errno, errval)
pymysql.err.OperationalError: (1054, "Unknown column 'products.product_name' in 'field list'")

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\protocols\http\httptools_impl.py", line 416, in run_asgi
    result = await app(  # type: ignore[func-returns-value]
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        self.scope, self.receive, self.send
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\middleware\proxy_headers.py", line 60, in __call__
    return await self.app(scope, receive, send)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\applications.py", line 1135, in __call__
    await super().__call__(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\applications.py", line 107, in __call__
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 186, in __call__
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 164, in __call__
    await self.app(scope, receive, _send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\exceptions.py", line 63, in __call__
    await wrap_app_handling_exceptions(self.app, conn)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\middleware\asyncexitstack.py", line 18, in __call__
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 716, in __call__ 
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 736, in app      
    await route.handle(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 290, in handle   
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 119, in app        
    await wrap_app_handling_exceptions(app, request)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 105, in app        
    response = await f(request)
               ^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 426, in app        
    raw_response = await run_endpoint_function(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    ...<3 lines>...
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 314, in run_endpoint_function
    return await run_in_threadpool(dependant.call, **values)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\concurrency.py", line 32, in run_in_threadpool
    return await anyio.to_thread.run_sync(func)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\to_thread.py", line 61, in run_sync    
    return await get_async_backend().run_sync_in_worker_thread(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        func, args, abandon_on_cancel=abandon_on_cancel, limiter=limiter
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 2525, in run_sync_in_worker_thread
    return await future
           ^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 986, in run
    result = context.run(func, *args)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\products.py", line 25, in list_products
    return query.all()
           ~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\query.py", line 2704, in all  
    return self._iter().all()  # type: ignore
           ~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\query.py", line 2857, in _iter
    result: Union[ScalarResult[_T], Result[_T]] = self.session.execute(
                                                  ~~~~~~~~~~~~~~~~~~~~^
        statement,
        ^^^^^^^^^^
        params,
        ^^^^^^^
        execution_options={"_sa_orm_load_options": self.load_options},
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\session.py", line 2351, in execute
    return self._execute_internal(
           ~~~~~~~~~~~~~~~~~~~~~~^
        statement,
        ^^^^^^^^^^
    ...<4 lines>...
        _add_event=_add_event,
        ^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\session.py", line 2249, in _execute_internal
    result: Result[Any] = compile_state_cls.orm_execute_statement(
                          ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self,
        ^^^^^
    ...<4 lines>...
        conn,
        ^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\context.py", line 306, in orm_execute_statement
    result = conn.execute(
        statement, params or {}, execution_options=execution_options
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1419, in execute
    return meth(
        self,
        distilled_parameters,
        execution_options or NO_OPTIONS,
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\sql\elements.py", line 527, in _execute_on_connection
    return connection._execute_clauseelement(
           ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        self, distilled_params, execution_options
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1641, in _execute_clauseelement
    ret = self._execute_context(
        dialect,
    ...<8 lines>...
        cache_hit=cache_hit,
    )
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1846, in _execute_context
    return self._exec_single_context(
           ~~~~~~~~~~~~~~~~~~~~~~~~~^
        dialect, context, statement, parameters
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1986, in _exec_single_context
    self._handle_dbapi_exception(
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~^
        e, str_statement, effective_parameters, cursor, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 2363, in _handle_dbapi_exception
    raise sqlalchemy_exception.with_traceback(exc_info[2]) from e
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\base.py", line 1967, in _exec_single_context
    self.dialect.do_execute(
    ~~~~~~~~~~~~~~~~~~~~~~~^
        cursor, str_statement, effective_parameters, context
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\engine\default.py", line 952, in do_execute
    cursor.execute(statement, parameters)
    ~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 153, in execute    
    result = self._query(query)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\cursors.py", line 322, in _query     
    conn.query(q)
    ~~~~~~~~~~^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 575, in query  
    self._affected_rows = self._read_query_result(unbuffered=unbuffered)
                          ~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 826, in _read_query_result
    result.read()
    ~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 1203, in read  
    first_packet = self.connection._read_packet()
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\connections.py", line 782, in _read_packet
    packet.raise_for_error()
    ~~~~~~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\protocol.py", line 219, in raise_for_error
    err.raise_mysql_exception(self._data)
    ~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\pymysql\err.py", line 150, in raise_mysql_exception
    raise errorclass(errno, errval)
sqlalchemy.exc.OperationalError: (pymysql.err.OperationalError) (1054, "Unknown column 'products.product_name' in 'field list'")
[SQL: SELECT products.id AS products_id, products.product_name AS products_product_name, products.price AS products_price, products.category_id AS products_category_id
FROM products
WHERE products.category_id = %(category_id_1)s AND lower(products.product_name) LIKE lower(%(product_name_1)s)]
[parameters: {'category_id_1': 1, 'product_name_1': '%q%'}]
(Background on this error at: https://sqlalche.me/e/20/e3q8)
INFO:database:📦 DB session opened
INFO:products:➕ Creating product: laptop
INFO:database:📦 DB session closed
INFO:     127.0.0.1:64529 - "POST /products/ HTTP/1.1" 500 Internal Server Error
ERROR:    Exception in ASGI application
Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\protocols\http\httptools_impl.py", line 416, in run_asgi
    result = await app(  # type: ignore[func-returns-value]
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        self.scope, self.receive, self.send
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\middleware\proxy_headers.py", line 60, in __call__
    return await self.app(scope, receive, send)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\applications.py", line 1135, in __call__
    await super().__call__(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\applications.py", line 107, in __call__
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 186, in __call__
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 164, in __call__
    await self.app(scope, receive, _send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\exceptions.py", line 63, in __call__
    await wrap_app_handling_exceptions(self.app, conn)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\middleware\asyncexitstack.py", line 18, in __call__
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 716, in __call__ 
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 736, in app      
    await route.handle(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 290, in handle   
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 119, in app        
    await wrap_app_handling_exceptions(app, request)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 105, in app        
    response = await f(request)
               ^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 426, in app        
    raw_response = await run_endpoint_function(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    ...<3 lines>...
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 314, in run_endpoint_function
    return await run_in_threadpool(dependant.call, **values)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\concurrency.py", line 32, in run_in_threadpool
    return await anyio.to_thread.run_sync(func)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\to_thread.py", line 61, in run_sync    
    return await get_async_backend().run_sync_in_worker_thread(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        func, args, abandon_on_cancel=abandon_on_cancel, limiter=limiter
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 2525, in run_sync_in_worker_thread
    return await future
           ^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 986, in run
    result = context.run(func, *args)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\products.py", line 30, in create_product
    p = models.Product(**payload.model_dump())
  File "<string>", line 4, in __init__
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\state.py", line 596, in _initialize_instance
    with util.safe_reraise():
         ~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\util\langhelpers.py", line 224, in __exit__
    raise exc_value.with_traceback(exc_tb)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\state.py", line 594, in _initialize_instance
    manager.original_init(*mixed[1:], **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\decl_base.py", line 2179, in _declarative_constructor
    raise TypeError(
        "%r is an invalid keyword argument for %s" % (k, cls_.__name__)
    )
TypeError: 'slug' is an invalid keyword argument for Product
INFO:database:📦 DB session opened
INFO:products:➕ Creating product: string
INFO:database:📦 DB session closed
INFO:     127.0.0.1:54233 - "POST /products/ HTTP/1.1" 500 Internal Server Error
ERROR:    Exception in ASGI application
Traceback (most recent call last):
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\protocols\http\httptools_impl.py", line 416, in run_asgi
    result = await app(  # type: ignore[func-returns-value]
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        self.scope, self.receive, self.send
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\uvicorn\middleware\proxy_headers.py", line 60, in __call__
    return await self.app(scope, receive, send)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\applications.py", line 1135, in __call__
    await super().__call__(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\applications.py", line 107, in __call__
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 186, in __call__
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\errors.py", line 164, in __call__
    await self.app(scope, receive, _send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\middleware\exceptions.py", line 63, in __call__
    await wrap_app_handling_exceptions(self.app, conn)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\middleware\asyncexitstack.py", line 18, in __call__
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 716, in __call__ 
    await self.middleware_stack(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 736, in app      
    await route.handle(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\routing.py", line 290, in handle   
    await self.app(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 119, in app        
    await wrap_app_handling_exceptions(app, request)(scope, receive, send)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 53, in wrapped_app
    raise exc
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\_exception_handler.py", line 42, in wrapped_app
    await app(scope, receive, sender)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 105, in app        
    response = await f(request)
               ^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 426, in app        
    raw_response = await run_endpoint_function(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    ...<3 lines>...
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\fastapi\routing.py", line 314, in run_endpoint_function
    return await run_in_threadpool(dependant.call, **values)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\starlette\concurrency.py", line 32, in run_in_threadpool
    return await anyio.to_thread.run_sync(func)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\to_thread.py", line 61, in run_sync    
    return await get_async_backend().run_sync_in_worker_thread(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        func, args, abandon_on_cancel=abandon_on_cancel, limiter=limiter
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 2525, in run_sync_in_worker_thread
    return await future
           ^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\anyio\_backends\_asyncio.py", line 986, in run
    result = context.run(func, *args)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\products.py", line 30, in create_product
    p = models.Product(**payload.model_dump())
  File "<string>", line 4, in __init__
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\state.py", line 596, in _initialize_instance
    with util.safe_reraise():
         ~~~~~~~~~~~~~~~~~^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\util\langhelpers.py", line 224, in __exit__
    raise exc_value.with_traceback(exc_tb)
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\state.py", line 594, in _initialize_instance
    manager.original_init(*mixed[1:], **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\susaisup\Downloads\fastapi-log-main\.venv\Lib\site-packages\sqlalchemy\orm\decl_base.py", line 2179, in _declarative_constructor
    raise TypeError(
        "%r is an invalid keyword argument for %s" % (k, cls_.__name__)
    )
TypeError: 'slug' is an invalid keyword argument for Product
