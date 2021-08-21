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
ms.openlocfilehash: 18d3296dfab4a28ba818199d0b9329888c692f55831bced2af5abedfd1f205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984064"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





