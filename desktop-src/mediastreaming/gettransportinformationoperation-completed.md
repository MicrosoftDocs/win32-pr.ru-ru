---
title: Жеттранспортинформатионоператион завершенное свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жеттранспортинформатионасинк.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жеттранспортинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жеттранспортинформатионоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735787"
---
# <a name="gettransportinformationoperationcompleted-property"></a>Свойство Жеттранспортинформатионоператион:: Completed

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттранспортинформатионоператион**](gettransportinformationoperation.md)
</dt> </dl>

 

 