---
title: Жетмутеоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетмутеасинк.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетмутеоператион
- API потоковой передачи мультимедиа интерфейса Жетмутеоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb27715f284b96af4ba9e6cf8ff825a7237ba027d46d30d77859018d4d8b5574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100678"
---
# <a name="getmuteoperationcompleted-property"></a>Жетмутеоператион. Completed, свойство

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетмутеоператион**](getmuteoperation.md)
</dt> </dl>

 

 