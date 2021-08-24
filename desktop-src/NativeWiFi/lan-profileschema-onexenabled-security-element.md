---
description: Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Онексенаблед (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801094"
---
# <a name="onexenabled-security-element"></a>Онексенаблед (Security), элемент

Элемент **онексенаблед** (Security) указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 x. Если **онексенаблед** имеет значение false, служба автоматической настройки никогда не использует 802.1 x для проверки подлинности портов. Если **онексенаблед** имеет значение true, служба автоматической настройки пытается выполнить проверку подлинности порта с помощью 802.1 x.

Этот элемент является необязательным. Значение по умолчанию — TRUE. Если **онексенаблед** не указан в профиле, для проверки подлинности порта может использоваться 802.1 x.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

Элемент **онексенаблед** определяется элементом [**Security**](lan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**бюллетеня**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**безопасность (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




