---
description: Метод onframes должен быть реализован монитором. МКСВК вызывает этот метод, когда буфер записи полон или время обновления прошло.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Метод Имонитор:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779174"
---
# <a name="imonitoronframes-method"></a>Метод Имонитор:: onframe

Метод **Onframes** должен быть реализован монитором. МКСВК вызывает этот метод, когда буфер записи полон или время обновления прошло.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Событие* \[ окне\]
</dt> <dd>

[Обновление \_ Структура событий](update-event.md) , содержащая сведения о кадрах, используемые для обновления событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка). МКСВК передает возвращаемое значение обратно в НПП для обработки.

Если метод завершается неудачно, возвращаемое значение является кодом ошибки. МКСВК передает возвращаемое значение обратно в НПП для обработки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




