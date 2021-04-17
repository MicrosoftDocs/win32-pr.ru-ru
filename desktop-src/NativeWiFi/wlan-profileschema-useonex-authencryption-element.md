---
description: Указывает, используется ли проверка подлинности 802.1 X.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Усеонекс (Аусенкриптион), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673919"
---
# <a name="useonex-authencryption-element"></a>Усеонекс (Аусенкриптион), элемент

Элемент Усеонекс (Аусенкриптион) указывает, используется ли проверка подлинности 802.1 X.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, использующих элемент **усеонекс** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Аусенкриптион (безопасность)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




