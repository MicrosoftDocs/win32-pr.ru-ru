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
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683836"
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



## <a name="remarks"></a>Комментарии

Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы политики локальной сети](lan-policyschema-elements.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 




