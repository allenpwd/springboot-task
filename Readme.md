##异步方法
让spring自动在新线程中处理调用的方法
- 配置类上标注@EnableSync：开启异步注解功能
- 在方法上标注@Sync：声明该方法是异步方法

##定时任务
- 配置类上标注@EnableScheduling：开启定时任务功能
- 在方法上标注@Scheduled并设置cron表达式
####cron表达式
second(秒), minute（分）, hour（时）, day of month（日）, month（月）, day of week（周几）
- second：0-59       ,-*/
- minute：0-59       ,-*/
- hour：0-23     ,-*/
- day of month：1-31     ,-*?/LWC
- month：1-12        ,-*/
- day of week：0-7或SUN-SAT,0和7是SUN       ,-*?/LC#

这里的day of week和quarts框架的规则不一样，quarts取值1-7：1是周日2是周一


##邮件任务
- 引入spring-boot-starter-mail
- JavaMailSenderImpl
