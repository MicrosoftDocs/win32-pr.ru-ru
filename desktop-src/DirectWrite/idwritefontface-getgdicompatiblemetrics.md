---
title: Идвритефонтфаце Жетгдикомпатиблеметрикс, метод
description: Получает единицы проектирования и общие метрики для начертания шрифта. Эти метрики применимы ко всем глифам в фонтфаце и используются приложениями для вычисления макета.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Непосредственная запись метода Жетгдикомпатиблеметрикс
- Прямая запись метода Жетгдикомпатиблеметрикс, интерфейс Идвритефонтфаце
- Прямая запись интерфейса Идвритефонтфаце, метод Жетгдикомпатиблеметрикс
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290714"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Метод Идвритефонтфаце:: Жетгдикомпатиблеметрикс

Получает единицы проектирования и общие метрики для начертания шрифта. Эти метрики применимы ко всем глифам в фонтфаце и используются приложениями для вычисления макета.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*емсизе* 
</dt> <dd>

Тип: **float**

Логический размер шрифта в единицах DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Тип: **float**

Число физических пикселов на DIP.

</dd> <dt>

*Преобразование* \[ в необязательное\]
</dt> <dd>

Тип: **[**дврите \_ Матрица**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \* const**

Необязательное преобразование, применяемое к глифам и их позициям. Это преобразование применяется после масштабирования, заданного размером шрифта и *pixelsPerDip*.

</dd> <dt>

*фонтфацеметрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **дврите \_ . \_ метрики шрифта**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Указатель на структуру [**\_ \_ метрики шрифта дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)для заполнения. Метрики, возвращаемые этой функцией, находятся в единицах дизайна шрифта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Стандартный код ошибки HRESULT.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

