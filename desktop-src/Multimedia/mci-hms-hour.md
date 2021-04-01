---
title: Макрос MCI_HMS_HOUR (МЦиапи. h)
description: Макрос MCI \_ ХМс \_ Hour извлекает компонент часов из параметра, содержащего сведения о упакованных часах/минутах/секундах (ХМс).
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072003"
---
# <a name="mci_hms_hour-macro"></a>\_Макрос MCI ХМс \_ часа

Макрос **MCI \_ ХМс \_ Hour** извлекает компонент часов из параметра, содержащего сведения о упакованных часах/минутах/секундах (ХМс).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двхмс* 
</dt> <dd>

Время в формате ХМС.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает компонент часов указанной информации ХМС.

## <a name="remarks"></a>Комментарии

Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды. Наиболее значимый байт не используется.

Макрос **MCI \_ ХМс \_ Hour** определяется следующим образом:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Макросы MCI](mci-macros.md)
</dt> </dl>

 

 





