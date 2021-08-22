---
title: Событие Рендерингпараметерсупдате
description: Возникает при обновлении любого из набора параметров элемента управления отрисовки в ДМР.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API потоковой передачи мультимедиа для события Рендерингпараметерсупдате
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08956baf37b0bf8bc2323138e5cad24d587a88af7283d52985559a8a8538571d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342934"
---
# <a name="renderingparametersupdate-event"></a>Событие Рендерингпараметерсупдате

Возникает при обновлении любого из набора параметров элемента управления отрисовки в ДМР.

## <a name="syntax"></a>Синтаксис


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**рендерингпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) с помощью метода [**Add \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 