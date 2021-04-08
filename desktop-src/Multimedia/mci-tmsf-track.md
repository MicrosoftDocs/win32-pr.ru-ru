---
title: Макрос MCI_TMSF_TRACK (МЦиапи. h)
description: Макрос MCI \_ тмсф \_ Track извлекает компонент треки из параметра, содержащего сведения о упакованных дорожках/минутах/сек/Frames (тмсф).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892049"
---
# <a name="mci_tmsf_track-macro"></a>\_Макрос MCI тмсф \_ Track

Макрос **MCI \_ тмсф \_ Track** извлекает компонент треки из параметра, содержащего сведения о упакованных дорожках/минутах/сек/Frames (тмсф).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двтмсф* 
</dt> <dd>

Время в формате ТМСФ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает компонент дорожек указанной информации ТМСФ.

## <a name="remarks"></a>Комментарии

Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.

Макрос **MCI \_ тмсф \_ Track** определяется следующим образом:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





