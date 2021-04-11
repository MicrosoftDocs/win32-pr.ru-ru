---
title: Макрос MCI_HMS_MINUTE (МЦиапи. h)
description: Макрос MCI \_ ХМс \_ Minute извлекает компонент минут из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137586"
---
# <a name="mci_hms_minute-macro"></a>\_Макрос MCI ХМс \_ Minute

Макрос **MCI \_ ХМс \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_HMS_MINUTE(
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

Возвращает компонент минут указанной информации ХМС.

## <a name="remarks"></a>Комментарии

Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды. Наиболее значимый байт не используется.

Макрос **MCI \_ ХМс \_ Minute** определяется следующим образом:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
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

 

 





