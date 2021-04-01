---
title: Жетмутеоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетмутеасинк.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетмутеоператион
- API потоковой передачи мультимедиа интерфейса Жетмутеоператион, метод Results
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133747"
---
# <a name="getmuteoperationgetresults-method"></a>Жетмутеоператион. results, метод

Возвращает результаты асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Значение выключения. Значение true указывает, что звук в данный момент выключен. Значение false указывает, что звук не отключен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетмутеоператион**](getmuteoperation.md)
</dt> </dl>

 

