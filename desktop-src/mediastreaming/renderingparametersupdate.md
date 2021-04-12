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
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337092"
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

## <a name="remarks"></a>Комментарии

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**рендерингпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) с помощью метода [**Add \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ рендерингпараметерсупдате**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 