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
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412861"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>Жетстреампропертиесоператион. Completed, свойство

Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетстреампропертиесасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Значение свойства

Обработчик событий.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетстреампропертиесоператион**](getstreampropertiesoperation.md)
</dt> </dl>

 

 