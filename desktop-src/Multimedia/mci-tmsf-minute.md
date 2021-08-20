---
title: Макрос MCI_TMSF_MINUTE (МЦиапи. h)
description: Макрос MCI \_ тмсф \_ Minute извлекает компонент минут из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE макрос Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673295aa92503c28ff7a285182fa9e5b1a71321dc59ab9a76536692adc836273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986125"
---
# <a name="mci_tmsf_minute-macro"></a>\_Макрос MCI тмсф \_ Minute

Макрос **MCI \_ тмсф \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_TMSF_MINUTE(
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

Возвращает компонент минут указанной информации ТМСФ.

## <a name="remarks"></a>Remarks

Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.

Макрос **MCI \_ тмсф \_ Minute** определяется следующим образом:


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
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

 

 





