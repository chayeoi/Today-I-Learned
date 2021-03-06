# NAT(Network Address Translation)

사설 IP 주소를 쓰고 있는 각각의 컴퓨터들이 외부의 인터넷에 접속할 수 있는 것은 바로 NAT(Network address translation)라는 기술 덕분이다. 사설 IP 주소를 갖고 있는 컴퓨터가 외부 인터넷에 접속을 한다면 내부적으로는 다음과 같은 과정을 거친다.

1. 사설 IP에 연결된 컴퓨터는 Gateway address에 해당하는 라우터에 요청 신호를 보낸다.
2. 라우터는 해당 요청이 내부 네트워크에 연결된 기기에 대한 요청인지를 확인한다.
3. 내부 네트워크에 대한 요청이 아니므로 라우터는 해당 요청을 WAN을 통해서 외부로 보낼 준비를 한다.
   1. 해당 요청이 어떤 사설 IP를 갖고 있는 기기가 보낸 요청인지를 내부적으로 기록한다.
   2. 요청을 보낸 기기가 갖고 있는 사설 IP 주소는 외부에서는 접속할 수 없는 주소이므로, 라우터의 NAT이라는 기술을 통해 요청한 사설 IP 주소를 공용 IP 주소로 변경한다.
4. 라우터는 외부 인터넷으로 요청을 보낸다.
5. 인터넷 상에서 요청을 전달받은 컴퓨터는 요청을 보냈던 라우터로 응답을 보낸다.
6. 라우터는 응답받은 정보를 확인한 후, 내부 네트워크 상에서 실제로 응답을 받아야 하는 기기에게 응답을 전송한다.

## 참고 {docsify-ignore}

* [NAT (Network address translation) | 생활코딩](https://opentutorials.org/course/3265/20035)
