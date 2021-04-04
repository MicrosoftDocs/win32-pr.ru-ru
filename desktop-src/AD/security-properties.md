---
title: Атрибуты безопасности пользователя
description: В дополнение к свойствам именования для объектов User, например objectGUID, objectSid, CN, distinguishedName и т. д., существуют другие свойства безопасности, используемые для входа в систему, доступа к сети и контроля доступа.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Атрибуты безопасности, использование AD
- Атрибуты безопасности пользователя AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2020
ms.locfileid: "103987965"
---
# <a name="user-security-attributes"></a>Атрибуты безопасности пользователя

В дополнение к свойствам именования для объектов User, например [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**CN**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)и т. д., существуют другие свойства безопасности, используемые для входа в систему, доступа к сети и контроля доступа. Эти свойства используются системой безопасности Windows 2000. Эти свойства можно просматривать и управлять с помощью оснастки Active Directory пользователи и компьютеры.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

Атрибут [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) указывает, когда истекает срок действия учетной записи. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC). Значение **тимек \_ бесконечно** (определено в лмакцесс. h) указывает, что срок действия учетной записи никогда не истекает.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**алтсекуритидентитиес**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

Атрибут [**алтсекуритидентитиес**](/windows/desktop/ADSchema/a-altsecurityidentities) — это атрибут с несколькими значениями, который содержит сопоставления для сертификатов X. 509 или внешних учетных записей пользователей Kerberos этому пользователю в целях проверки подлинности. Различные пакеты безопасности, включая пакет проверки подлинности с открытым ключом и Kerberos, используют эти данные для проверки подлинности пользователей, если они представляют альтернативную форму идентификации, например сертификат, билет Kerberos для UNIX и т. д. Создайте маркер Windows 2000 на основе соответствующей учетной записи пользователя, чтобы получить доступ к системным ресурсам.

Для сертификатов X. 509 значения должны быть именами издателя и субъекта в сертификатах 509v3, выданных внешним общедоступным центром сертификации, который соответствует учетной записи пользователя, используемой для поиска учетной записи для проверки подлинности. Пакет SSL (Schannel) использует следующий синтаксис: X509: <somecertinfotype> сомецертинфо. Например, следующее значение указывает имя издателя " \<I\> " с различающимся именем "c = US, O = интернетка, CN = апубликцертификатеаусорити" и именем субъекта " \<S\> " с различающимся именем "c = US, o = Fabrikam, OU = Sales, CN = Джефф Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Имейте в виду, что \<S\> поддерживаются "" или "" \<I> и " \<S\> ". Наличие только " \<I\> " не поддерживается. Приложения не должны изменять значения в " \<I\> " или " \<S\> ", так как частичное сопоставление DN не поддерживается.

Для внешних учетных записей Kerberos значения должны быть именем учетной записи Kerberos. Пакет Kerberos использует следующий синтаксис: "Kerberos: Митаккаунтнаме". Например, ниже приведено значение для учетной записи в Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**Аргументы badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Не реплицируется. Атрибут [**аргументы badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) указывает время последнего попытки пользователя войти в учетную запись с помощью неправильного пароля. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC). Этот атрибут сохраняется отдельно на каждом контроллере домена в домене. Нулевое значение означает, что время последнего неправильного пароля неизвестно. Чтобы получить точное значение времени последнего неправильного пароля пользователя в домене, необходимо запросить каждый контроллер домена в домене и использовать максимальное значение.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Не реплицируется. Атрибут [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) указывает, сколько раз пользователь пытался войти в учетную запись, используя неверный пароль. Этот атрибут сохраняется отдельно на каждом контроллере домена в домене. Значение 0 указывает, что значение неизвестно. Чтобы получить точное значение для общего числа неудачных попыток ввода пароля в домене, необходимо запросить каждый контроллер домена в домене и использовать сумму значений.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Страница**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

Атрибут [**codepage**](/windows/desktop/ADSchema/a-codepage) указывает кодовую страницу для выбранного пользователем языка. Это значение не используется в Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**каунтрикоде**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

Атрибут [**каунтрикоде**](/windows/desktop/ADSchema/a-countrycode) указывает код страны или региона для языка пользователя. Это значение не используется в Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

Атрибут [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) задает путь к корневому каталогу для пользователя. Строка может иметь значение null.

Если [**хомедриве**](/windows/desktop/ADSchema/a-homedrive) задано и указывает букву диска, [**ХОМЕДИРЕКТОРИ**](/windows/desktop/ADSchema/a-homedirectory) должен быть UNC-путем. Путь должен представлять собой сетевой UNC-путь к \\ \\ \\ общему \\ каталогу сервера форм. Это значение может быть пустой строкой.

Если [**хомедриве**](/windows/desktop/ADSchema/a-homedrive) не задан, то [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) должен быть локальным путем, например C: \\ милокалдир.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**хомедриве**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

Атрибут [**хомедриве**](/windows/desktop/ADSchema/a-homedrive) указывает букву диска, с которой должен СОПОСТАВЛЯТЬся UNC-путь, заданный параметром **хомедиректори**. Буква диска должна быть указана в следующем формате:


```C++
<drive letter>:
```



где " \<drive letter\> " — буква диска для сопоставлений. Пример:


```C++
Z:
```



Если этот атрибут не задан, [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) должен быть локальным путем, например, C: \\ милокалдир.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**ластлогофф**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Не реплицируется. Атрибут [**ластлогофф**](/windows/desktop/ADSchema/a-lastlogoff) указывает, когда выполнялся последний выход из системы. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC). Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** . Этот атрибут сохраняется отдельно на каждом контроллере домена в домене. Нулевое значение означает, что время последнего выхода из системы неизвестно. Чтобы получить точное значение последнего выхода пользователя из системы в домене, необходимо запросить каждый контроллер домена в домене и использовать максимальное значение.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**ластлогон**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Не реплицируется. Атрибут [**ластлогон**](/windows/desktop/ADSchema/a-lastlogon) указывает, когда выполнялся последний вход в систему. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC). Большая часть этого большого целого числа соответствует элементу **двхигхдатетиме** структуры [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , а нижняя часть соответствует элементу **двловдатетиме** структуры **fileTime** . Этот атрибут сохраняется отдельно на каждом контроллере домена в домене. Нулевое значение означает, что время последнего входа неизвестно. Чтобы получить точное значение для последнего входа пользователя в домен, необходимо запросить каждый контроллер домена в домене и использовать максимальное значение.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**лмпвдхистори**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

Атрибут [**лмпвдхистори**](/windows/desktop/ADSchema/a-lmpwdhistory) — это журнал паролей пользователя в формате LAN Manager (LM), который является односторонним форматом (OWF). LM OWF используется для обеспечения совместимости с клиентами LAN Manager 2. x, Windows 95 и Windows 98. Этот атрибут используется только операционной системой. Имейте в виду, что нельзя наследовать пароль в виде обычного текста из формы OWF пароля.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**логонкаунт**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Не реплицируется. Атрибут [**логонкаунт**](/windows/desktop/ADSchema/a-logoncount) подсчитывает количество успешных попыток входа пользователя в эту учетную запись. Этот атрибут поддерживается на каждом контроллере домена в домене. Значение 0 указывает, что значение неизвестно. Чтобы получить точное значение общего числа успешных попыток входа в домен, необходимо запрашивать каждый контроллер домена в домене и использовать сумму значений.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**доступа**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

Атрибут [**mail**](/windows/desktop/ADSchema/a-mail) является атрибутом с одним значением, который содержит SMTP-адрес пользователя, например " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**максстораже**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

Атрибут [**максстораже**](/windows/desktop/ADSchema/a-maxstorage) указывает максимальный объем дискового пространства, который может использовать пользователь. Чтобы использовать все доступное дисковое пространство, используйте параметр **\_ максстораже \_ неограниченный пользователем** (определенный в лмакцесс. h).

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**Групп**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

Атрибут [**memberof**](/windows/desktop/ADSchema/a-memberof) является многозначным атрибутом, который содержит группы, в которых пользователь является прямым элементом, за исключением первичной группы, представленной [**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid). Членство в группе зависит от контроллера домена, от которого извлекается этот атрибут:

-   На КОНТРОЛЛЕРе домена, который содержит пользователя, [**член memberOf**](/windows/desktop/ADSchema/a-memberof) для пользователя завершается по отношению к членству в группах в этом домене; Однако **член memberOf** не содержит членства пользователя в локальных и глобальных группах домена в других доменах.
-   На сервере GC [**член memberOf**](/windows/desktop/ADSchema/a-memberof) для пользователя завершается относительно членства в универсальных группах.

Если для контроллера домена справедливы оба условия, оба набора данных содержатся в [**memberof**](/windows/desktop/ADSchema/a-memberof).

Имейте в виду, что этот атрибут перечисляет группы, содержащие пользователя в атрибуте Member, но не содержит рекурсивный список вложенных предшественников. Например, если пользователь O является членом группы C, а Группа B и Группа B были вложены в группу A, атрибут [**memberof**](/windows/desktop/ADSchema/a-memberof) пользователя O перечислит группу C и группу B, но не группу a.

Этот атрибут не хранится — он является вычисленным атрибутом ссылки.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**нтпвдхистори**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

Атрибут [**нтпвдхистори**](/windows/desktop/ADSchema/a-ntpwdhistory) — это журнал паролей пользователя в одностороннего формата Windows NT (OWF). Windows 2000 использует Windows NT OWF. Этот атрибут используется только операционной системой. Имейте в виду, что нельзя получить пароль в формате обычного текста из формы OWF пароля.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**осермаилбокс**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

Атрибут [**осермаилбокс**](/windows/desktop/ADSchema/a-othermailbox) является многозначным атрибутом, который содержит другие дополнительные адреса электронной почты в форме, например "Ккмаил: жеффсмис".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**пассвордекспиратиондате**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

Дата истечения срока действия пароля не является атрибутом объекта пользователя. Это вычисляемое значение, основанное на сумме [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) для пользователя и [**макспвдаже**](/windows/desktop/ADSchema/a-maxpwdage) домена пользователя. Чтобы получить дату истечения срока действия пароля, получите свойство [**IADsUser. пассвордекспиратиондате**](/windows/desktop/ADSI/iadsuser-property-methods) . Этот атрибут нельзя изменить для пользователя. Вместо этого задайте свойство [**иадсдомаин. макспассвордаже**](/windows/desktop/ADSI/iadsdomain-property-methods) , чтобы изменить параметр для домена.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

Атрибут [**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid) является атрибутом с одним значением, который содержит [**примариграуптокен**](/windows/desktop/ADSchema/a-primarygrouptoken) группы, которая является основной группой объекта. Основная группа объекта не включается в атрибут [**memberof**](/windows/desktop/ADSchema/a-memberof) . Например, по умолчанию основной группой объекта пользователя является **примариграуптокен** группы «Пользователи домена», но группа «Пользователи домена» не является частью атрибута « **memberof** » объекта пользователя.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**Путь к пути**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

Атрибут [**FilePath**](/windows/desktop/ADSchema/a-profilepath) указывает путь к профилю пользователя. Это значение может быть пустой строкой, локальным абсолютным путем или UNC-путем.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

Атрибут [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) указывает время последнего изменения пароля. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).

Система использует значение этого атрибута и атрибут [**макспвдаже**](/windows/desktop/ADSchema/a-maxpwdage) домена, который содержит объект User, для вычисления даты окончания срока действия пароля. То есть сумма [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) для пользователя и **макспвдаже** домена пользователя.

Этот атрибут определяет, должен ли пользователь изменять пароль при следующем входе пользователя в систему. Если [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) равен нулю, по умолчанию пользователь должен сменить пароль при следующем входе в систему. Значение-1 указывает, что пользователю не нужно менять пароль при следующем входе в систему. Система устанавливает это значение равным-1 после того, как пользователь задает пароль.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

Атрибут [**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) задает целое число, представляющее тип счета. Это значение задается операционной системой при создании объекта.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

Атрибут [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath) задает путь к файлу скрипта входа пользователя, cmd, exe или bat. Строка может иметь значение null.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

Атрибут [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) — это пароль пользователя.

Чтобы задать пароль пользователя, используйте метод [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) , если ваш скрипт или приложение позволяет пользователю изменить свой пароль или метод [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) , если ваш сценарий или приложение разрешает администратору сбрасывать пароль.

Пароль пользователя в одностороннего формата Windows NT (OWF). Windows 2000 использует Windows NT OWF. Этот атрибут используется только операционной системой. Имейте в виду, что нельзя получить пароль в формате обычного текста из формы OWF пароля.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

Атрибут [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) задает флаги, управляющие поведением пароля, блокировки, отключения и включения, а также поведения сценариев и домашнего каталога для пользователя. Этот атрибут также содержит флаг, указывающий тип учетной записи объекта. Обычно для объекта пользователя \_ \_ задана обычная учетная запись УФ.

Следующие флаги определены в Лмакцесс. h.



| Flag                     | Описание                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_сценарий УФ               | Сценарий входа выполнен. Это значение должно быть установлено для LAN Manager 2,0 или Windows NT.                                                                             |
| УФ \_ аккаунтдисабле       | Учетная запись пользователя отключена.                                                                                                                                    |
| \_требуется УФ хомедир \_    | Требуется корневой каталог. Это значение не учитывается в Windows NT и Windows 2000.                                                                            |
| УФ \_ PASSWD \_ нотрекд      | Пароль не требуется.                                                                                                                                         |
| УФ \_ PASSWD не \_ удается \_ изменить | Пользователь не может изменить пароль.                                                                                                                             |
| \_Блокировка УФ              | Учетная запись в данный момент заблокирована. Это значение можно очистить, чтобы разблокировать ранее заблокированную учетную запись. Это значение нельзя использовать для блокировки ранее заблокированной учетной записи. |
| УФ \_ не с \_ истекшим сроком действия \_ PASSWD | Представляет пароль, срок действия которого никогда не истекает для учетной записи.                                                                                               |



 

Следующие флаги описывают тип учетной записи. Можно задать только одно значение. Изменить тип учетной записи нельзя.



| Flag                            | Описание                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Обычная \_ учетная запись УФ             | Это тип учетной записи по умолчанию, представляющий обычного пользователя.                                                                                                                                                                                  |
| УФ \_ временная \_ \_ учетная запись повторения    | Это учетная запись для пользователей, Первичная учетная запись которых находится в другом домене. Эта учетная запись предоставляет пользователю доступ к этому домену, но не к домену, который доверяет данному домену. Диспетчер пользователей ссылается на этот тип учетной записи в качестве учетной записи локального пользователя. |
| \_ \_ учетная запись доверия рабочей станции УФ \_ | Это учетная запись компьютера для сервера Windows NT Workstation/Windows 2000 Professional или Windows NT Server или Windows 2000, которая является членом этого домена.                                                                                     |
| \_ \_ \_ учетная запись доверия сервера УФ      | Это учетная запись компьютера для контроллера домена резервного копирования Windows NT, который является членом этого домена.                                                                                                                                           |
| \_ \_ учетная запись междоменного доверия УФ \_ | Это позволяет доверять учетной записи домена Windows NT, который доверяет другим доменам.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

Атрибут [**USERCERTIFICATE**](/windows/desktop/ADSchema/a-usercertificate) является многозначным атрибутом, который содержит сертификаты X509v3, закодированные в DER-кодировке, выданные пользователю. Имейте в виду, что этот атрибут содержит сертификаты открытого ключа, выданные этому пользователю в службе сертификации Майкрософт.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**усершаредфолдер**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

Атрибут [**усершаредфолдер**](/windows/desktop/ADSchema/a-usersharedfolder) указывает UNC-путь к папке общих документов пользователя. Путь должен представлять собой сетевой UNC-путь к \\ \\ \\ общему \\ каталогу сервера форм. Это значение может быть пустой строкой.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**усерворкстатионс**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

Атрибут [**усерворкстатионс**](/windows/desktop/ADSchema/a-userworkstations) — это однозначный атрибут, содержащий NetBIOS-имена рабочих станций, на которые пользователь может выполнять вход. Каждое NetBIOS-имя разделяются запятыми.

Если значения не заданы, это означает, что ограничения отсутствуют. Чтобы отключить вход с этой учетной записи со всех рабочих станций, задайте \_ значение УФ аккаунтдисабле (определено в лмакцесс. h) в атрибуте [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

</dd> </dl>

 

 
