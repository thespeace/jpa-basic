# 객체와 테이블 매핑
JPA에서 가장 중요한 것 중 하나는 엔티티와 테이블을 정확하게 매핑하는 것이다.  
따라서 매핑 어노테이션을 숙지해야 하는데, 아래의 4가지로 분류할 수 있다.

* 객체와 테이블 매핑: ```@Entity```, ```@Table```
* 필드와 컬럼 매핑: ```@Column```
* 기본 키 매핑: ```@Id```
* 연관관계 매핑: ```@ManyToOne```, ```@JoinColumn```

<br>

### ```@Entity```
* ```@Entity```가 붙은 클래스는 JPA가 관리, 엔티티라 한다.
* JPA를 사용해서 테이블과 매핑할 클래스는 ```@Entity```가 필수다.
* 속성: name
  * ex) ```@Entity(name = "Member")``` 
  * JPA에서 사용할 엔티티 이름을 지정한다.
  * 기본값: 클래스 이름을 그대로 사용(예: Member)
  * 같은 클래스 이름이 없으면 가급적 기본값을 사용한다.
* **주의**
  * 기본 생성자 필수(파라미터가 없는 public 또는 protected 생성자)
  * final 클래스, enum, interface, inner 클래스에는 사용 불가
  * 저장할 필드에 final 사용 불가