---
title: Жетстреампропертиесоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетстреампропертиесасинк.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетстреампропертиесоператион
- API потоковой передачи мультимедиа интерфейса Жетстреампропертиесоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6fc6982866ed97f70467d13cb5e899d94a1459266ca0149d12400d154aad784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100668"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>Жетстреампропертиесоператион. Completed, свойство

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетстреампропертиесасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетстреампропертиесоператион**](getstreampropertiesoperation.md)
</dt> </dl>

 

 