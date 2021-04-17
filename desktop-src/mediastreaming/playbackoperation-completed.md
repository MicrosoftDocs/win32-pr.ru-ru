---
title: Плайбаккоператион. Completed, свойство
description: Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной одним из методов воспроизведения Медиарендерер.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Плайбаккоператион
- API потоковой передачи мультимедиа интерфейса Плайбаккоператион, завершенное свойство
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710191"
---
# <a name="playbackoperationcompleted-property"></a>Плайбаккоператион. Completed, свойство

Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной одним из методов воспроизведения [**медиарендерер**](mediarenderer.md) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**плайбаккоператион**](playbackoperation.md)
</dt> </dl>

 

 




