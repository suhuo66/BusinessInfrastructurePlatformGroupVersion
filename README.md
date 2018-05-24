# BusinessInfrastructurePlatformGroupVersion

<h2>Run</h2>
<code>clean org.springframework.boot:spring-boot-maven-plugin:run -q -e</code>

<h2>License</h2>
BusinessInfrastructurePlatformGroupVersion is Open Source software released under the <a href="https://opensource.org/licenses/Apache-2.0">Apache 2.0 license</a>
<p>Copyright (c) 2017-present Mingshu Jian</p>


使用Spring Data JPA + QueryDSL + Hibernate。
基本的增删改查和调用存储过程通过Spring Data JPA Repository来解决
稍微复杂的查询或是批量操作使用QueryDSL或Spring Data Specification的API来解决
特别特别复杂的查询操作可以使用Spring Data JPA Repository的注解定义native sql来解决
所有持久层底层操作都由Hibernate来支持，且为了保证效率和性能，不需要的包/特性就不需要引入，基本上使用core包就能够解决问题，当然如果有需要可以加上orm

全过程脱离任何格式(.java除外)的配置文件，都使用Java Config的方式进行配置，除了需要抽象出一套自己架构的持久层的API以外，只需要提供一个独立的空内容.java配置文件(如果不需要多数据源配置的话)，在类上面配置RepositoryFactoryBean和Repository接口包路径全使用过程中，除了native sql处以外，全部持久层操作都是类型安全的，特别是使用QueryDSL或Specification后...

从此，mybatis根本就没有存在的必要...PS: 推荐在Spring Boot基础上进行构建，毕竟有插排和没有插排构架起来在效率和性能上是截然不同的...
