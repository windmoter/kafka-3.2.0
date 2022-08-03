
- https://velog.io/@doublejone831/Kafka2-%EC%B9%B4%ED%94%84%EC%B9%B4-%ED%99%98%EA%B2%BD-%EA%B5%AC%EC%84%B1%ED%95%98%EA%B8%B0
# zookeeper 실행
start/b D:\kafka_2.13-3.2.0\bin\windows\zookeeper-server-start.bat D:\kafka_2.13-3.2.0\config\zookeeper.properties

# kafka 실행
start/b D:\kafka_2.13-3.2.0\bin\windows\kafka-server-start.bat D:\kafka_2.13-3.2.0\config\server.properties
# Topic생성하기 <topic-name>
D:\kafka_2.13-3.2.0\bin\windows\kafka-topics.bat --create --topic topic_name --bootstrap-server localhost:9092
# Console-Producer로 메세지 보내기-> 프롬프트3
D:\kafka_2.13-3.2.0\bin\windows\kafka-console-producer.bat --topic topic_name --bootstrap-server localhost:9092

# Console-Consumer로 메세지 확인-> 프롬프트4
D:\kafka_2.13-3.2.0\bin\windows\kafka-console-consumer.bat --topic topic_name --from-beginning --bootstrap-server localhost:9092

- https://blog.naver.com/PostView.nhn?blogId=sharplee7&logNo=222127972098
# kafka-demo
아파치 카프카를 이용한 Pub/Sub 구조의 심플한 테스트입니다.

kafka-pub의 KafkaPubApplication을 실행 시키고
kafka-sub의 KafkaSubApplication을 실행 시키도록 합니다.

KafkaPubApplcation의 api테스트 페이지인 http://localhost:8081/swagger-ui.html으로 로그인해 API를 테스트 하면
입력된 값이 KafkaSubApplication의 콘솔에 전달 되는 것을 확인 할 수 있습니다.