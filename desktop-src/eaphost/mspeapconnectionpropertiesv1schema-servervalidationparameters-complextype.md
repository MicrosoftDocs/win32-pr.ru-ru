---
title: Сложный тип Сервервалидатионпараметерс (PEAP)
description: Сведения о сложном типе Сервервалидатионпараметерс. Этот тип содержит сведения о выполнении проверки сервера. | Сложный тип Сервервалидатионпараметерс (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
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
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000052"
---
# <a name="servervalidationparameters-complex-type-peap"></a>Сложный тип Сервервалидатионпараметерс (PEAP)

Сложный тип **сервервалидатионпараметерс** содержит сведения о выполнении проверки сервера.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                                                    | Тип        | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | Логическое     | Указывает, должен ли пользователь запрашивать проверку сервера. <br/> Если [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение true, PEAP выполняет проверку сервера без ввода данных пользователем. Если проверка завершается неудачно, PEAP не проверяет подлинность.<br/> Если [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (ЦС).<br/> Элемент [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) является необязательным.<br/> |
| [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | complexType | Представляет список серверов, которым доверяет клиент. Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями. <br/> Элемент [**ServerName**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**трустедрутка**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary   | Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. <br/> Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.<br/> Элемент [**трустедрутка**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) является необязательным.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a>Атрибуты



| Имя                    | Тип    | Описание                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| перформсервервалидатион | Логическое | Windows 7 или более поздней версии: указывает, выполняется ли проверка сервера. Элемент [**перформсервервалидатион**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) является необязательным.<br/> |



## <a name="requirements"></a>Требования



| Роль | Минимальная поддерживаемая версия ОС |
|------|------------------------------|
| Клиент<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Сервер<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Сложные типы схемы mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[**акцептсервернаме**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





