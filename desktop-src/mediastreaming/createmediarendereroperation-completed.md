---
title: Креатемедиарендерероператион. Completed, свойство
description: Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной Креатемедиарендерерасинк или Креатемедиарендерерфромбасикдевицеасинк.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Креатемедиарендерероператион
- API потоковой передачи мультимедиа интерфейса Креатемедиарендерероператион, завершенное свойство
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783954"
---
# <a name="createmediarendereroperationcompleted-property"></a>Креатемедиарендерероператион. Completed, свойство

Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**креатемедиарендерерасинк**](imediarendererfactory-createmediarendererasync.md) или [**креатемедиарендерерфромбасикдевицеасинк**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**креатемедиарендерероператион**](createmediarendereroperation.md)
</dt> </dl>

 

 




