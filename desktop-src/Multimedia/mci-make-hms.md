---
title: Макрос MCI_MAKE_HMS (МЦиапи. h)
description: '\_ \_ Макрос make ХМс создает значение времени в формате "Упакованные часы/минуты/секунды (ХМс)" из заданных значений часов, минут и секунд.'
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS макрос Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056605b0148abad27f9911d2e6db4687ca7d65be55075433940814b62ea844ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986371"
---
# <a name="mci_make_hms-macro"></a>\_Макрос make \_ ХМс

Макрос **\_ make \_ ХМс** создает значение времени в формате "Упакованные часы/минуты/секунды (ХМс)" из заданных значений часов, минут и секунд.

## <a name="syntax"></a>Синтаксис


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*hours* 
</dt> <dd>

Количество часов.

</dd> <dt>

*minutes* 
</dt> <dd>

Количество минут.

</dd> <dt>

*секунд* 
</dt> <dd>

Количество секунд.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает время в упакованном формате ХМС.

## <a name="remarks"></a>Remarks

Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды. Наиболее значимый байт не используется.

Макрос **\_ make \_ ХМс для MCI** определяется следующим образом:


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Макросы MCI](mci-macros.md)
</dt> </dl>

 

 





