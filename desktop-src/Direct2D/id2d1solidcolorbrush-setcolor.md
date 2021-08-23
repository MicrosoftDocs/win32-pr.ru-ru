---
title: ID2D1SolidColorBrush Сетколор методы
description: Задает цвет сплошной кисти цвета.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Методы Сетколор Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eb281265a9567db5da6252944fa1da1a6beb1bd4a0fb2a6a4d80ef1177455fc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873954"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>Методы ID2D1SolidColorBrush:: Сетколор

Задает цвет сплошной кисти цвета.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                          | Описание                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**Сетколор (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Задает цвет кисти с сплошным цветом. <br/> |
| [**Сетколор (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Задает цвет сплошной кисти цвета. <br/> |



## <a name="remarks"></a>Remarks

Чтобы облегчить создание цветов, Direct2D предоставляет класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) . Он предлагает несколько вспомогательных методов для создания цветов и предоставляет набор или стандартные цвета.

## <a name="examples"></a>Примеры

В следующем коде показано, как использовать этот метод.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

