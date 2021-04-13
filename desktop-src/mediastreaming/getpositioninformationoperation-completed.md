---
title: Жетпоситионинформатионоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетпоситионинформатионасинк.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетпоситионинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жетпоситионинформатионоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412929"
---
# <a name="getpositioninformationoperationcompleted-property"></a>Жетпоситионинформатионоператион. Completed, свойство

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетпоситионинформатионоператион**](getpositioninformationoperation.md)
</dt> </dl>

 

 