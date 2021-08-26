---
title: Макрос MCI_MSF_MINUTE (МЦиапи. h)
description: Макрос MCI \_ MSF \_ Minute извлекает компонент минут из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE макрос Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8423e63c7e155c072b496a9bf13c332619f96e8c6780cac6fae266f6a924c9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039144"
---
# <a name="mci_msf_minute-macro"></a>Макрос для платформы MCI ( \_ \_ минуту)

Макрос **MCI \_ MSF \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).

## <a name="syntax"></a>Синтаксис


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двмсф* 
</dt> <dd>

Время в формате MSF.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает компонент минут указанной информации MSF.

## <a name="remarks"></a>Remarks

Время в формате MSF выражается в виде значения **типа DWORD** с наименьшим значащим байтом, содержащим минуты, следующим наименее значащим байтом, содержащим секунды, и следующим наименьшим значащим байтом, содержащим кадры. Наиболее значимый байт не используется.

Макрос **MCI \_ MSF \_ Minute** определяется следующим образом:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a>Requirements (Требования)



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

 

 





