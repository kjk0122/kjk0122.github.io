---
layout: post
title:  "오늘 한 일"
date:   2023-07-05 17:27:00 +0900
categories: jekyll update
---

@Configuration은 빈을 등록할 수 있는 어노테이션 중 하나이다.

@Configuration 어노테이션을 사용하면, 하나 이상의 @Bean이 붙은 메서드가 포함된 빈 설정용 클래스를 만들 수 있다.
스프링 컨테이너는 @Bean이 붙은 메서드를 통해 빈을 생성한다.

ApplicationContext는 @Configuration이 붙은 클래스 내부에서 @Bean이 붙은 메서드들을 찾는다.

@Bean 이 붙은 메서드들은 자바 객체를 반환하는 메서드이다.
반환된 자바 객체는 스프링 컨테이너에 빈으로 등록된다.
빈의 이름은 @Bean이 붙은 메서드 이름이 된다. (이 코드의 경우 메서드명과 같은 myBean 빈이 생성된다.)


```
@Configuration
public class Config {

    @Bean
    public MyBean myBean() {
        return new MyBean();
    }
}
```
