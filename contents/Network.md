# 2.Network
**:radio_button: Contents**
* [OSI 7계층](#osi-7계층)
* [TCP/IP](#tcp-ip의-개념)
* [TCP와 UDP](#tcp와-udp)
* [TCP와 UDP의 헤더 분석](#tcp와-udp의-헤더-분석)

*********
### OSI 7계층
* OSI 7계층이란?
  * OSI 7 계층은 네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말한다. 
  * 통신이 일어나는 과정을 단계별로 파악할 수 있다. (한눈에 알아보기 쉽다. & easy for troubleshooting the network problems)
  
  <img src="./image/Network/osi.png" width="60%" height="60%"> 

* OSI 7계층 단계
  * 1. Physical Layer
    * 전기적, 기계적 기능적 특성을 이용하여 통신 케이블로 데이터를 전송함
    * 통신단위는 비트이며, 1과 0, 즉 전기적으로 On / Off를 나타낸다
    * physical layer에서는 데이터를 전송만 할뿐, 그 데이턱 무엇인지, 어떤 에러가 있는지는 신경쓰지 않는다.
    * 통신장비, 리피터, 허브 등
  
  * 2. DataLink Layer
    * 물리계층을 통해 송수신되는 정보의 오류와 흐름을 관리 -> 안전한 정보의 전달을 도와줌
    * DataLink Layer에서는 맥 주소를 통해 통신함. 전송되는 단위는 프레임이다.
    * DataLink Layer에서는 point to point 간 신뢰성 있는 전송을 보장하기 위한 계층으로 CRC 기반의 오류 제어와 흐름 제어가 필요
    * 주소 값은 물리적으로 할당 받는다. 이는 네트워크 카드가 만들어질 때부터 맥 주소(MAC address)가 정해져 있다는 뜻
    * 이더넷이 대표적인 예
