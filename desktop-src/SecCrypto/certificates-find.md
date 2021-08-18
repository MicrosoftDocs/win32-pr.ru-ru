---
description: Возвращает объект Certificates, который содержит все сертификаты, соответствующие указанным условиям поиска.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'Метод ICertificates2:: Find'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100994"
---
# <a name="icertificates2find-method"></a>Метод ICertificates2:: Find

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Find** возвращает объект [**Certificates**](certificates.md) , который содержит все сертификаты, соответствующие указанным условиям поиска. Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*FindType* \[ окне\]
</dt> <dd>

Значение перечисления [**\_ \_ \_ типа CAPICOM Certificate Find**](capicom-certificate-find-type.md) , которое указывает тип критерия соответствия, указанный в параметре *варкритериа* . В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                                                                        | Значение                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ Certificate \_ найти \_ \_ хэш SHA1**</dt> </dl>                              | Возвращает сертификаты с хэшем SHA1, который соответствует хэшу SHA1, указанному в параметре *варкритериа* .<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**CAPICOM \_ Certificate \_ найти \_ имя субъекта \_**</dt> </dl>                     | Возвращает сертификаты, имена субъектов которых полностью или частично соответствуют имени субъекта, указанному в параметре *варкритериа* . Этот вызов выполняет поиск только в поле "имя субъекта".<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**CAPICOM \_ Certificate \_ найти \_ \_ имя издателя**</dt> </dl>                        | Возвращает сертификаты, имя издателя которых полностью или частично совпадает с именем издателя, указанным в параметре *варкритериа* . Этот вызов выполняет поиск только в поле имени издателя.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**\_ \_ \_ имя корневого узла поиска CAPICOM Certificate \_**</dt> </dl>                              | Возвращает сертификаты, имя корневого субъекта которых полностью или частично совпадает с корневым именем субъекта, указанным в параметре *варкритериа* . Этот вызов создает цепочку. Этот вызов выполняет поиск в поле имени субъекта корневого сертификата.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**\_ \_ \_ имя шаблона поиска CAPICOM \_ Certificate**</dt> </dl>                  | Возвращает сертификаты, имя шаблона которых совпадает с именем шаблона, указанным в параметре *варкритериа* .<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**\_ \_ найти расширение CAPICOM \_ Certificate**</dt> </dl>                               | Возвращает сертификаты с расширением, которое соответствует расширению, указанному в параметре *варкритериа* .<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**\_ \_ \_ Расширенное свойство поиска CAPICOM Certificate \_**</dt> </dl>      | Возвращает сертификаты в хранилище, которые явно содержат расширенное свойство со значением, указанным в параметре *варкритериа* .<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**CAPICOM \_ Certificate \_ найти \_ \_ политику приложения**</dt> </dl>   | Возвращает сертификаты в хранилище, которые имеют расширение расширенного использования ключа, расширение политики приложения или расширенное свойство, указанное в параметре *варкритериа* .<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**CAPICOM \_ Certificate \_ Поиск \_ \_ политики сертификата**</dt> </dl>   | Возвращает сертификаты, содержащие OID политики в расширении политики сертификатов, указанном в параметре *варкритериа* .<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**\_ \_ \_ допустимое время поиска CAPICOM Certificate \_**</dt> </dl>                           | Возвращает сертификаты, время которых допустимо.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**\_ \_ \_ недействительное время \_ \_ \_ поиска CAPICOM Certificate**</dt> </dl> | Возвращает сертификаты, время которых еще не является допустимым.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**\_время поиска CAPICOM Certificate истекло \_ \_ \_**</dt> </dl>                     | Возвращает сертификаты, время которых истекло.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**\_Использование CAPICOM Certificate \_ Поиск \_ ключа \_**</dt> </dl>                              | Возвращает сертификаты, содержащие сведения об использовании ключей в расширении Кэйусаже, указанном в параметре *варкритериа* . Если расширение Кэйусаже отсутствует, все использование ключа считается недоступным.<br/>                           |



 

</dd> <dt>

*варкритериа* \[ в необязательное\]
</dt> <dd>

Вариант, содержащий условия поиска. Эти данные должны соответствовать типу данных, указанных в параметре *FindType* . Если параметр *FindType* имеет значение " \_ \_ допустимое время поиска CAPICOM Certificate" \_ , " \_ \_ недействительное время поиска элемента CAPICOM Certificate" \_ \_ \_ \_ \_ или \_ \_ \_ \_ "не передается", а значение этого параметра не указано, то предполагается текущее время. Примеры для каждого типа данных см. в разделе Примечания. Значение по умолчанию — 0.

</dd> <dt>

*бфиндвалидонли* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, возвращаются ли только допустимые сертификаты. Значение по умолчанию — false. Это означает, что возвращаются все сертификаты, соответствующие условиям поиска.

Если значение — true, поиск не будет возвращать следующие типы сертификатов:

-   Сертификаты, время действия которых истекло или которые еще не действительны.
-   Сертификаты не связаны должным образом.
-   Сертификаты с проблемами подписи.
-   Отозванные сертификаты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**Certificates**](certificates.md) , содержащий результаты поиска.

**CAPICOM 2,1:** Возвращаемый объект [**Certificates**](certificates.md) содержит ссылки на сертификаты в коллекции, в которой был выполнен поиск. Все изменения, внесенные в сертификаты в возвращенном объекте **Certificate** , отражаются в этой коллекции.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 и CAPICOM 2.0.0.3:** Возвращаемый объект [**Certificates**](certificates.md) содержит копии сертификатов в коллекции, в которой был выполнен поиск. Любые изменения, внесенные в сертификаты в возвращенном объекте **Certificates** , не отражаются в этой коллекции.

## <a name="remarks"></a>Remarks

В следующих примерах показаны возможные условия поиска для различных типов условий поиска.



| *FindType* , параметр                              | *варкритериа* , параметр                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ Certificate \_ найти \_ \_ хэш SHA1            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| CAPICOM \_ Certificate \_ найти \_ имя субъекта \_         | "Намеофперсон"                                                                                                                     |
| CAPICOM \_ Certificate \_ найти \_ \_ имя издателя          | Компанией                                                                                                                         |
| \_ \_ \_ имя корневого узла поиска CAPICOM Certificate \_            | "Корневой центр Майкрософт"                                                                                                         |
| \_ \_ \_ имя шаблона поиска CAPICOM \_ Certificate        | "Аутоенроллефс"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| \_ \_ найти расширение CAPICOM \_ Certificate             | "2.5.29.31"<br/> \_ \_ \_ расширение использования ключа объекта \_ CAPICOM<br/> "Список рассылки списка отзыва сертификатов"<br/>                           |
| \_ \_ \_ Расширенное свойство поиска CAPICOM Certificate \_    | \_ \_ \_ сведения о Prov ключе CAPICOM PropID \_                                                                                                   |
| CAPICOM \_ Certificate \_ найти \_ \_ политику приложения   | 1.3.6.1.5.5.7.3.3<br/> 1.3.6.1.5.5.7.3.4<br/> \_EKU для \_ \_ проверки подлинности сервера CAPICOM OID \_<br/> "Подписывание кода"<br/> |
| CAPICOM \_ Certificate \_ Поиск \_ \_ политики сертификата   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Корпоративные высокие гарантии"<br/>                                                           |
| \_ \_ \_ допустимое время поиска CAPICOM Certificate \_           | \#04/15/2002, 6:00 РМ\#                                                                                                            |
| \_ \_ \_ недействительное время \_ \_ \_ поиска CAPICOM Certificate | \#04/15/2002, 6:00 РМ\#                                                                                                            |
| \_время поиска CAPICOM Certificate истекло \_ \_ \_         | \#04/15/2002, 6:00 РМ\#                                                                                                            |
| \_Использование CAPICOM Certificate \_ Поиск \_ ключа \_            | Использование элемента CAPICOM \_ шифрования паролей \_ только для \_ ключа \_                                                                                                |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сертификаты**](certificates.md)
</dt> <dt>

[**CAPICOM \_ OID**](capicom-oid.md)
</dt> </dl>

 

 
