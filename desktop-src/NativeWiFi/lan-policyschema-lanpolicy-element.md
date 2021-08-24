---
description: Содержит политику проводной локальной сети.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Ланполици, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 468e9fb0500c4a514b7b0a9dddea023f0851b9f7ba783504548f2285810ffffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780184"
---
# <a name="lanpolicy-element"></a>Ланполици, элемент

Элемент Ланполици содержит политику проводной локальной сети. Этот элемент является уникальным корневым элементом для профиля политики проводных сетей.

Целевое пространство имен для элемента **ланполици** — `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип                                                     | Описание                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**nописание**](lan-policyschema-description-lanpolicy-element.md)             | [**наметипе**](lan-policyschema-nametype-simpletype.md) | Содержит описание политики проводной локальной сети. <br/>                                                                                                                          |
| [**енаблеаутоконфиг**](lan-policyschema-enableautoconfig-globalflags-element.md) | Логическое                                                  | Указывает, используют ли компьютеры встроенную службу автоматической настройки для управления подключениями к проводным сетям, для которых требуется проверка подлинности уровня 2 (например, 802.1 X).<br/> |
| [**глобалфлагс**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Содержит глобальные параметры для автоматической настройки проводных сетей. <br/>                                                                                          |
| [**безымян**](lan-policyschema-name-lanpolicy-element.md)                           | [**наметипе**](lan-policyschema-nametype-simpletype.md) | Содержит имя политики проводной локальной сети. <br/>                                                                                                                                 |
| [**профилелист**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Содержит список профилей, применяемых на уровне домена или компьютера. <br/>                                                                                                |



## <a name="remarks"></a>Remarks

Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы политики локальной сети](lan-policyschema-elements.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 




