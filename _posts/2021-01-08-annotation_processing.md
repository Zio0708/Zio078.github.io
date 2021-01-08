---
title: "annotation processing 문제"
date: 2021-01-08 20:15:00 -0400
categories: error
---
문제 :

SpringBoot Gradle 에서 cannot find symbol method builder()
lombok을 설치했음에도 builder() 인식하지 못함

해결 : 
build.gradle() 파일내에
dependencies안에
annotationProcessor('org.projectlombok:lombok')
testAnnotationProcessor('org.projectlombok:lombok')
입력하니 해결됨

분석 : 
Annotation processing is a tool build in javac for scanning and processing annotations at compile time.
You can register your own annotation processor for certain annotations.
annotation을 사용하기위해서 설정해 주는것같다.
jdk 를 다른걸 쓰니까 설정이 달라서 그런것 같다.
