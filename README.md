# grpc_python(Calculator Program)
Basic gPRC introduction and implementation for python. 

To generate RPC classes(all files are located in a single folder and the commands are run in that same folder.)::

    $ pip install grpcio
    $ pip install grpcio-tools
    $ python -m grpc_tools.protoc -I. --python_out=. --grpc_python_out=. calculator.proto


The files generated will be as follows:

    calculator_pb2.py — contains message classes
    calculator_pb2.Number for request/response variables (x and y)
  
calculator_pb2_grpc.py — contains server and client classes

    calculator_pb2_grpc.CalculatorServicer for the server
    calculator_pb2_grpc.CalculatorStub for the client

start the server using the command,

    $ python server.py
    Starting server. Listening on port 50051.

With the server already listening, we simply run our client.

    $ python client.py
    6.0
## for more info visit
https://grpc.io/
