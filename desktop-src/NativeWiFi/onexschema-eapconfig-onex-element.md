---
description: Задает конфигурацию EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Элемент Еапконфиг (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663048"
---
# <a name="eapconfig-onex-element"></a>Элемент Еапконфиг (OneX)

Элемент **еапконфиг** (OneX) указывает конфигурацию EAPHost.

В отличие от большинства элементов в схеме профиля 802.1 X, этот элемент находится в `https://www.microsoft.com/provisioning/EapHostConfig` пространстве имен. Его дочерние элементы определяются в [схеме еафостконфиг](../eaphost/eaphostconfigschema-schema.md). Элемент [**еафостконфиг**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) является дочерним по отношению к элементу **еапконфиг** .

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **еапконфиг** определяется элементом [**OneX**](onexschema-onex-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> </dl>

 

 
