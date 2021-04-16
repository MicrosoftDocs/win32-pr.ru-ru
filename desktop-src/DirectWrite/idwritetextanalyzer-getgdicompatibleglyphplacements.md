---
title: Идвритетекстанализер Жетгдикомпатиблеглифплацементс, метод
description: Поместите выходные данные глифов из метода "методы" в соответствии со шрифтами и правилами отрисовки системы записи.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Непосредственная запись метода Жетгдикомпатиблеглифплацементс
- Прямая запись метода Жетгдикомпатиблеглифплацементс, интерфейс Идвритетекстанализер
- Прямая запись интерфейса Идвритетекстанализер, метод Жетгдикомпатиблеглифплацементс
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665266"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Метод Идвритетекстанализер:: Жетгдикомпатиблеглифплацементс

Поместите выходные данные глифов [**из метода "методы" в соответствии**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) со шрифтами и правилами отрисовки системы записи.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*текстстринг* \[ окне\]
</dt> <dd>

Тип: **const WCHAR \***

Массив символов, содержащий исходную строку, из которой поступили глифы.

</dd> <dt>

*клустермап* \[ окне\]
</dt> <dd>

Тип: **const UINT16 \***

Указатель на сопоставление между диапазонами символов и диапазонами глифов. Он возвращается символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*текстпропс* \[ окне\]
</dt> <dd>

Тип: **[ **дврите \_ изменение \_ \_ свойств текста**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Указатель на массив структур, который содержит свойства формирования для каждого символа. Эта структура возвращается символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textLength* 
</dt> <dd>

Тип: **UINT32**

Длина текста *текстстринг*.

</dd> <dt>

*глифиндицес* \[ окне\]
</dt> <dd>

Тип: **const UINT16 \***

Массив индексов глифов [**, возвращаемых символами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*глифпропс* \[ окне\]
</dt> <dd>

Тип: **константа \* [**формирования дврите \_ \_ \_ свойств глифа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**

Указатель на массив структур, который содержит свойства формирования для каждого глифа, возвращаемого символами- [**глифами**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*глифкаунт* 
</dt> <dd>

Тип: **UINT32**

Число глифов, возвращаемых из [**Подглифов**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*фонтфаце* \[ окне\]
</dt> <dd>

Тип: **[ **идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Указатель на начертание шрифта, которое является источником для выходных глифов.

</dd> <dt>

*фонтемсизе* 
</dt> <dd>

Тип: **float**

Логический размер шрифта в DIP.

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

 *в сторону* 
</dt> <dd>

Тип: **bool** .

Логический флаг, установленный в **значение true** , если текст должен отображаться вертикально.

</dd> <dt>

 *исригхттолефт* 
</dt> <dd>

Тип: **bool** .

Логический флаг, установленный в **значение true** для текста справа налево.

</dd> <dt>

 *скриптаналисис* \[ окне\]
</dt> <dd>

Тип: " **const [**дврите" \_ \_ анализ скриптов**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Указатель на результат анализа скрипта из вызова [**анализескрипт**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .

</dd> <dt>

 *localeName* \[ в необязательное\]
</dt> <dd>

Тип: **const WCHAR \***

Массив символов, содержащий языковой стандарт, используемый при выборе глифов. Например, один и тот же символ может сопоставляться с разными глифами для ja-JP и zh-CHS. Если это **значение равно NULL**, используется сопоставление по умолчанию, основанное на скрипте.

</dd> <dt>

 *функции* \[ в необязательное\]
</dt> <dd>

Тип: **const [**дврите \_ типографские \_ функции**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Массив указателей на наборы типографских функций для использования в каждом диапазоне функций.

</dd> <dt>

 *феатуреранжеленгсс* \[ в необязательное\]
</dt> <dd>

Тип: **const UINT32 \***

Длина каждого диапазона компонентов в символах. Сумма всех значений длины должна быть равна *TextLength*.

</dd> <dt>

 *феатуреранжес* 
</dt> <dd>

Тип: **UINT32**

Число диапазонов функций.

</dd> <dt>

 *глифадванцес* \[ заполняет\]
</dt> <dd>

Тип: **float \***

При возврате из этого метода содержит предварительную ширину каждого глифа.

</dd> <dt>

 *глифоффсетс* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ \_ смещение глифа дврите**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

При возврате из этого метода содержит смещение начала каждого глифа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритетекстанализер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

