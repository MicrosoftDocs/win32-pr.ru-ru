---
description: Метод Сенднмевент отправляет события в инструментарий управления Windows (WMI) (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Метод Имониторевентер:: Сенднмевент (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673424"
---
# <a name="imonitoreventersendnmevent-method"></a>Метод Имониторевентер:: Сенднмевент

Метод **сенднмевент** отправляет события в инструментарий управления Windows (WMI) (WMI).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнмевентдата* \[ окне\]
</dt> <dd>

Указатель на событие, переданное в WMI.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ ОК.

Если метод завершился неудачно, возвращаемое значение НМЕРР не \_ хватает \_ \_ памяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




