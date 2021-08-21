---
title: Метод BasicDevice.remove_ConnectionStatusChanged
description: Отменяет регистрацию обработчика событий для события Коннектионстатусчанжед. | Метод BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API потоковой передачи мультимедиа remove_ConnectionStatusChanged метода
- API потоковой передачи remove_ConnectionStatusChanged метода, интерфейс Басикдевице
- API потоковой передачи мультимедиа интерфейса Басикдевице, метод remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89057195c23aa917c7338a8abb740817bb6af7896261cf1d31bcb37d5d5d5ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972503"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a>Басикдевице. Remove \_ коннектионстатусчанжед, метод

Отменяет регистрацию обработчика событий для события [**коннектионстатусчанжед**](connectionstatuschanged.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*токен* \[ окне\]
</dt> <dd>

Ссылка на маркер, полученный из метода [**Add \_ коннектионстатусчанжед**](basicdevice-add-connectionstatuschanged.md) при регистрации обработчика событий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**басикдевице**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

