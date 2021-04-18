---
description: Указывает тип устройства планшета, например перо, мышь или сенсорно-чувствительный дигитайзер.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Перечисление TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674392"
---
# <a name="tablet_device_kind-enumeration"></a>\_Перечисление типов планшетных устройств \_

Указывает тип устройства планшета, например перо, мышь или сенсорно-чувствительный дигитайзер.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**мышь ПЛАНШЕТного \_ устройства \_**
</dt> <dd>

Планшет — это мышь. Сюда входят сенсорные панели, находящиеся на многих ноутбуках.

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**перо ПЛАНШЕТного \_ устройства \_**
</dt> <dd>

Планшет использует электромагнитное перо и дигитайзер.

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_ \_ сенсорный ввод устройств**
</dt> <dd>

Планшет использует сенсорно-чувствительный дигитайзер.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Метод ITablet2:: Жетдевицекинд**](itablet2-getdevicekind.md)
</dt> </dl>

 

 




