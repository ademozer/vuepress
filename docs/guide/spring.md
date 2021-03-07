# Spring Notları

## Spring Vault

[Spring Vault][vault]

[Vault Nedir?][vault_hashi]

![Vault][vault_resim]

## Spring Security

Spring Security yi ayarlamak için 
@EnableWebSecurity annotasyonu kullanılır.

```
    @EnableWebSecurity
    public class WebSecurity extends WebSecurityConfigurerAdapter {
	    @Override
	    protected void configure(HttpSecurity http) throws Exception { 
	        http
	        .cors().and()
	        .csrf().disable().authorizeRequests()
	        .antMatchers("/users").hasRole("manager")
	        .anyRequest().authenticated()
	        .and()
	        .formLogin();
	    }
    }
```
örnekler 
- [Spring Securityde Kullanıcı Detaylarının Getirilmesi](https://www.baeldung.com/get-user-in-spring-security)
   ```
       Authentication authentication = SecurityContextHolder.getContext().getAuthentication();
       String currentPrincipalName = authentication.getName();
   ```   
- [Spring Security Örnek - 2](https://www.journaldev.com/2736/spring-security-example-userdetailsservice)
- [Spring Security Örnek - 3](https://github.com/Baeldung/spring-security-registration)
- [Spring Security Örnek - 4](https://memorynotfound.com/spring-security-basic-authentication-configuration-example/) 
- [Spring Security Örnek - 5](https://www.journaldev.com/2736/spring-security-example-userdetailsservice)
- [Spring Security Örnek - 6](https://www.appsdeveloperblog.com/spring-security-default-username-password-role/)

## Spring - Soap

Her ne kadar REST teknolojisi SOAP teknolojinin yerine geçmeye başlamışsa da bazı projelerde hala SOAP ile çalışmak gerekmektedir. 
Spring dünyasında *Spring WS* bu iş için kullanılabilirse de en iyi uygulama *Apache CXF* kullanımıdır.
Apache CXF kullanırken JPA servisi kullanmak istersek @Autowired yerine @Resource annaotasyonunu kullanmalıyız.
<https://stackoverflow.com/questions/52190817/spring-boot-cxf-service-throws-an-exception-with-jpa>
örnek: 

```
   public class ProductWebFormImpl implements ProductWebFormService {
	@Resource  
	ProductWebFormServices productWebFormServices;
	@Override
	public List<ProductWebFormDto> productWebFormList(String agentCode) {
		return productWebFormServices.productWebFormList(agentCode);
	}

}
```





[vault]: https://spring.io/projects/spring-vault
[vault_adesk]: https://knowledge.autodesk.com/support/vault-products/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/Vault-About/files/GUID-87D9CA09-9881-4506-9465-0677392BCD7E-htm.html 
[vault_resim]: https://help.autodesk.com/cloudhelp/2019/ENU/Vault-About/images/GUID-3B186A85-CCD8-41C2-B518-817C279B9054.png
[vault_hashi]: https://learn.hashicorp.com/vault

