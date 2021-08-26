---
title: Элемент Еаптипе (mspeapuserpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: e27923d77a36b917b3356b7c5c79d408bc0a99d49d70967677b56a9047ed0b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067184"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a>Элемент Еаптипе (mspeapuserpropertiesv1schema)

Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType
        "
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
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                               | Тип                                                                                      | Описание                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Протокола**](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | Элемент [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) определяет внутренний метод и учетные данные для использования с этим методом. Если конфигурация PEAP настроена для гостевого доступа по протоколу PEAP, этот элемент отсутствует.<br/>                                  |
| [**пеапекстенсионс**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [**пеапекстенсионстипе**](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | Элемент [**пеапекстенсионс**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) обеспечивает будущие улучшения схемы. <br/> Элемент [**пеапекстенсионс**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) является необязательным.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





