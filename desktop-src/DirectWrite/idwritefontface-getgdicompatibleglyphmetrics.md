---
title: Идвритефонтфаце Жетгдикомпатиблеглифметрикс, метод
description: Получает метрики глифов в единицах дизайна шрифта с возвращаемыми значениями, совместимыми с тем, что создает GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Непосредственная запись метода Жетгдикомпатиблеглифметрикс
- Прямая запись метода Жетгдикомпатиблеглифметрикс, интерфейс Идвритефонтфаце
- Прямая запись интерфейса Идвритефонтфаце, метод Жетгдикомпатиблеглифметрикс
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668861"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Метод Идвритефонтфаце:: Жетгдикомпатиблеглифметрикс

Получает метрики глифов в единицах дизайна шрифта с возвращаемыми значениями, совместимыми с тем, что создает GDI.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*емсизе* 
</dt> <dd>

Тип: **float**

Размер гическая шрифта в DIP.

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

*усегдинатурал* 
</dt> <dd>

Тип: **bool** .

Если задано **значение false**, метрики совпадают с метриками текста с псевдонимами GDI. Если задано **значение true**, метрики совпадают с метриками текста, ИЗМЕРЯЕМыми GDI, с использованием шрифта, созданного с помощью **технологии CLEARTYPE для \_ естественного \_ качества**.

</dd> <dt>

*глифиндицес* \[ окне\]
</dt> <dd>

Тип: **const UINT16 \***

Массив индексов глифов, для которых нужно вычислить метрики.

</dd> <dt>

*глифкаунт* 
</dt> <dd>

Тип: **UINT32**

Число элементов в массиве *глифиндицес* .

</dd> <dt>

*глифметрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ \_ метрики глифов дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Массив структур [**\_ \_ метрик глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) , заполняемый этой функцией. Метрики находятся в единицах дизайна шрифта.

</dd> <dt>

*в сторону* 
</dt> <dd>

Тип: **bool** .

Логическое значение, указывающее, используется ли шрифт в параллельном исполнении. Это может повлиять на метрики глифов, если шрифт имеет наклонное моделирование, поскольку имитация наклона в сторону отличается от ненаправленного наклонного моделирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Стандартный код ошибки **HRESULT** . Если любой из входных индексов глифов находится за пределами допустимого диапазона индекса глифа для текущего начертания шрифта, возвращается значение **E \_ INVALIDARG** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

