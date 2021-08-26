---
title: Элемент Еаптипе (eaptlsuserpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: fbc58ab640b7993d274abdb134de4648d51c495c07f70a4468460de1d920bd76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021634"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Элемент Еаптипе (eaptlsuserpropertiesv1schema)

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
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
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



| Элемент                                                                   | Тип      | Описание                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Имен**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Захватывает имя пользователя для отправки в ответе EAP-Identity. Если элемент [**username**](eaptlsuserpropertiesv1schema-username-element.md) отсутствует, то EAP-TLS использует имя в сертификате, на который ссылается элемент [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .<br/> |
| [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.<br/>                                                                                                                                                                                                                             |



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

[Схема eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





