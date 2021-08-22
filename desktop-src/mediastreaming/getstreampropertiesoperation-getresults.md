---
title: Жетстреампропертиесоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетстреампропертиесасинк.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетстреампропертиесоператион
- API потоковой передачи мультимедиа интерфейса Жетстреампропертиесоператион, метод Results
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3520cc44919e9c606c6625c75193b5f1ab54f4005cc098316bd8769ad0e0fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735825"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>Жетстреампропертиесоператион. results, метод

Возвращает результаты асинхронной операции, запущенной [**жетстреампропертиесасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетстреампропертиесоператион**](getstreampropertiesoperation.md)
</dt> </dl>

 

