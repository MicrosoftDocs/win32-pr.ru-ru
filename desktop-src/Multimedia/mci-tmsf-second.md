---
title: Макрос MCI_TMSF_SECOND (МЦиапи. h)
description: '\_ \_ Второй макрос MCI тмсф извлекает компонент секунд из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).'
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND макрос Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92dc8f7771df35e9ddc712d263e805ba1e844ca42cde607d7204dc6dc7b350d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784203"
---
# <a name="mci_tmsf_second-macro"></a>\_ \_ Второй макрос MCI тмсф

**\_ \_ Второй макрос MCI тмсф** извлекает компонент секунд из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_TMSF_SECOND(
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

Возвращает компонент секунд указанной информации ТМСФ.

## <a name="remarks"></a>Remarks

Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.

**Второй макрос \_ тмсф \_ MCI** определяется следующим образом:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





