---
title: Сложный тип Сервервалидатионпараметерс (TLS)
description: Сведения о сложном типе Сервервалидатионпараметерс. Этот тип содержит сведения о выполнении проверки сервера. | Сложный тип Сервервалидатионпараметерс (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- Сервервалидатионпараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694024"
---
# <a name="servervalidationparameters-complex-type-tls"></a>Сложный тип Сервервалидатионпараметерс (TLS)

Сложный тип **сервервалидатионпараметерс** содержит сведения о выполнении проверки сервера.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                                                    | Тип      | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | Логическое   | Указывает, должен ли пользователь запрашивать проверку сервера. <br/> Если [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность. <br/> Если [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).<br/> Элемент [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) является необязательным.<br/> |
| [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | строка    | Представляет список серверов, которым доверяет клиент. Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями.<br/> Элемент [**ServerName**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**трустедрутка**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary | Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. <br/> Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.<br/> Элемент [**трустедрутка**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





