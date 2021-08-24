---
title: Стреамселектоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Селектбестстреамасинк.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Стреамселектоператион
- API потоковой передачи мультимедиа интерфейса Стреамселектоператион, завершенное свойство
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554874c19054f4b2ee46fbfe29fb4dfb8149e476ff96d040ffdbdd9b39de4612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847584"
---
# <a name="streamselectoperationcompleted-property"></a>Стреамселектоператион. Completed, свойство

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**селектбестстреамасинк**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**стреамселектоператион**](streamselectoperation.md)
</dt> </dl>

 

 