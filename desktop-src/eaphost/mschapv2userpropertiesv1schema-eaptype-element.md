---
title: Элемент Еаптипе (mschapv2userpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187749"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>Элемент Еаптипе (mschapv2userpropertiesv1schema)

Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип   | Описание                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Имен**](mschapv2userpropertiesv1schema-username-element.md)               |        | Указывает пользователя, для которого выполняется проверка подлинности. Если этот элемент отсутствует, имя пользователя получается из Winlogon. Элемент [**username**](mschapv2userpropertiesv1schema-username-element.md) является необязательным.<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | строка | Определяет домен пользователя или компьютера, для которого выполняется проверка подлинности. Если этот элемент отсутствует, используется домен из Winlogon. Элемент [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) является необязательным.<br/>        |
| [**Пароль**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | строка | Указывает пароль пользователя или компьютера, для которого выполняется проверка подлинности. Если этот элемент отсутствует, хэш пароля получается из Winlogon. Элемент [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) является необязательным.<br/> |



## <a name="remarks"></a>Remarks

Элемент **processContents** обеспечивает будущие улучшения схемы. Элемент **processContents** является необязательным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





