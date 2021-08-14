---
title: D1111 с использованием слоя, когда клип достаточно
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Слой используется с НУЛЕВой маской непрозрачности, непрозрачностью 1,0 и прямоугольной геометрической маской по оси. API-интерфейс обмена сообщениями Push/Pop должен добиться того же результата с более высокой производительностью.
keywords:
- D1111 с использованием слоя, когда Clip является достаточным Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b03a6c2a4806724cd7cfdc97354e29e86dc60e0f1729ee9efeca89d971ca0a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758104"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: использование слоя при наличии клипа

Производительность — слой используется с **нулевой** маской непрозрачности, непрозрачностью 1,0 и прямоугольной геометрической маской по оси. API-интерфейс обмена сообщениями Push/Pop должен добиться того же результата с более высокой производительностью.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Адрес интерфейса.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Уровень ошибки | Информация |



 

## <a name="examples"></a>Примеры

В следующем коде используется [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , если слой содержит только один примитив (прямоугольник), а для полей структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) задано значение по умолчанию. Значения по умолчанию для структуры **\_ \_ параметров слоя D2D1** см. в разделе [**лайерпараметер**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



В этом примере создается следующее сообщение отладки:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Возможные причины

Слой использовался, когда были бы достаточно методы [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) .

 

 