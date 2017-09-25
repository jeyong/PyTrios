PyTrios
=======

PyTrios 모듈은 TriOS 광학 센서와 시리얼 포트로 통신이 가능합니다.

지원 : 

-RAMSES SAM과 SAMIP 계열의 센서들(spectrometer 모듈만 해당하면 inclination/pressure 데이터는 현재 지원하지 않음)

-MicroFlu 센서(예로 Chl, PC, CDOM)

-IPS boxes 



이 소프트웨어는 공식 TriOS 제품이 아닙니다. 공식 TriOS 소프트웨어는 http://www.trios.de/ 를 방문해서 정보를 얻으세요.

통신 프로토콜을 구현하는 동안 TriOS의 지원에 감사를 표합니다.

특별히 보장하는 부분은 없으면 GPL license 대신 맥주를 사는 것도 가능합니다. 즐겨주세요.

----
설치 : 
 * serial
 * numpy
 * matplotlib

----
관련 문서 :
 * [TriOS RAMSES ](http://www.trios.de/index.php?eID=tx_nawsecuredl&u=0&g=0&t=1506217611&hash=32d2f0765b5cc3c2fbfa1fcf86f7951b3e41d726&file=uploads/tx_cccascatalog/files/d02-010en201704_brochure_ramses.pdf)

----
실행 : 
 * Rrs_example.py
   * __main__
     * Listen : 인자로 전달한 COM Port에서 listen
     * Query : ps.TCommandSend(query)를 이용해 query
     * loop

 * Query
   * ps.TCommandSend(query)를 이용해 query 전달

 * Packet Receive
   * TListen()
     * s2parse = _get_s2parse() //serial에서 stream 수신
     * packet = TPacket(s2parse) // packet으로 변환
     * handlePacket //packet 처리

