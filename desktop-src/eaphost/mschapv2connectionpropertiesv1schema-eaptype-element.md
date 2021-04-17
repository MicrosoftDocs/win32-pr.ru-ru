---
title: Элемент Еаптипе (mschapv2connectionpropertiesv1schema)
description: Является производным типом элемента Еаптипе из схемы baseeapconnectionpropertiesv1. Это верхний элемент, который отображается внутри элемента config схемы Еафостконфиг.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187761"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Элемент Еаптипе (mschapv2connectionpropertiesv1schema)

Элемент **еаптипе** является производным типом элемента [еаптипе](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) . Это верхний элемент, который отображается внутри элемента config схемы [еафостконфиг](eaphostconfigschema-elements.md)

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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



| Элемент                                                                                                       | Тип    | Описание                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**усевинлогонкредентиалс**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | Логическое | Управляет использованием учетных данных винлогин. Если значение — TRUE, EAP MS-CHAPv2 получает учетные данные из Winlogon. Если значение равно FALSE, то EAP MS-CHAPv2 получает учетные данные от пользователя. <br/> Элемент [**усевинлогонкредентиалс (еаптипе)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) является необязательным.<br/> |



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

[Схема mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





