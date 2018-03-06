•	The program performs the HTTP GET and PUT request, first the server is started and then the client is started. The server runs on port number 9000 and client on 9001.
•	The client accepts the input from the command line. Firstly, for GET instruction the command is given in the form of GET test.txt. on receiving this command, the server fetches the test.txt file from the server. And returns a response of 200 OK.
•	If the file is not found the server returns a response of 404.
•	for PUT request to be performed by the program the command to be given if PUT nithya.txt 6400, which performs HTTP PUT request by sending the text file nithya.txt file and a copy of it is saved under the name Client_test.txt on the server side.
DESIGN AND POSSIBLE IMPROVEMENTS:
GET REQUEST
•	For GET request the server opens a socket to receives the request from the client and on receiving the get request it sends back the file requested and opens a second port on which a GET request is accepted to generate a response to the request. This design opens a second socket to perform the GET request since my code had some complexities. This design may not be followed in real world applications. Which is a short come in my design and there is a scope for improvement.

PUT REQUEST

•	For PUT request the server opens a socket and receives the request from the client, the client sends PUT request along with the file and the port number on which the request must be executed. The file received on the server is saved. The program also prints the data stored in the file by converting it to string format. After the file is saved the server response with a response 200 OK. There is a delay to store the file and give display the output which can be improved. 
