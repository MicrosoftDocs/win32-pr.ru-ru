---
title: IDWriteFactory2 Креатеглифрунаналисис, метод
description: Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Непосредственная запись метода Креатеглифрунаналисис
- Прямая запись метода Креатеглифрунаналисис, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Креатеглифрунаналисис
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ea5c2dc4cb97b1b9ba02e786efc20a4e2a44990b9a1d28b862aeab254079a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048834"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Метод IDWriteFactory2:: Креатеглифрунаналисис

Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*glyphRun* \[ окне\]
</dt> <dd>

Тип: **[**\_ \_ выполнение**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \* константы дврите const**

Структура, указывающая свойства запуска глифа.

</dd> <dt>

*Преобразование* \[ в необязательное\]
</dt> <dd>

Тип: **[**дврите \_ Матрица**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \* const**

Необязательное преобразование, применяемое к глифам и их позициям. Это преобразование применяется после масштабирования, указанного в параметре Емсизе и pixelsPerDip.

</dd> <dt>

*рендерингмоде* 
</dt> <dd>

Тип: **\_ \_ режим рендеринга дврите**

Задает режим рендеринга, который должен быть одним из режимов растровой отрисовки (т. е. не является значением по умолчанию и не структурным).

</dd> <dt>

*меасурингмоде* 
</dt> <dd>

Тип: **[ **дврите \_ измерение \_ режим**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Задает метод для измерения глифов.

</dd> <dt>

*гридфитмоде* 
</dt> <dd>

Тип: **[ **дврите \_ \_ \_ режим вписывания в сетку**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Как поместить контур глифа в сетку. Это значение должно быть не по умолчанию.

</dd> <dt>

*антиалиасмоде* 
</dt> <dd>

Тип: **[ **дврите \_ \_ \_ режим сглаживания текста**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Задает режим сглаживания.

</dd> <dt>

*баселинеоригинкс* 
</dt> <dd>

Тип: **float**

Горизонтальное положение исходного плана в DIP.

</dd> <dt>

*баселинеоригини* 
</dt> <dd>

Тип: **float**

Вертикальное положение исходного плана в DIP.

</dd> <dt>

*глифрунаналисис* \[ заполняет\]
</dt> <dd>

Тип: **[ **идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Получает указатель на только что созданный объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

