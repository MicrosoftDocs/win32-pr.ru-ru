---
title: Событие Транспортпараметерсупдате
description: Происходит при каждом обновлении любого из наборов параметров транспорта в ДМР.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API потоковой передачи мультимедиа для события Транспортпараметерсупдате
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034522"
---
# <a name="transportparametersupdate-event"></a>Событие Транспортпараметерсупдате

Происходит при каждом обновлении любого из наборов параметров транспорта в ДМР.

## <a name="syntax"></a>Синтаксис


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**транспортпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) с помощью метода [**Add \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ транспортпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 