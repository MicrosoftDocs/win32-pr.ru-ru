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
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415801"
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

Тип: **const константа \* [**дврите \_ \_ Запуск**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)* _

Структура, указывающая свойства запуска глифа.

</dd> <dt>

_transform * \[ в, необязательно\]
</dt> <dd>

Тип: **const [**дврите \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Необязательное преобразование, применяемое к глифам и их позициям. Это преобразование применяется после масштабирования, указанного в параметре Емсизе и pixelsPerDip.

</dd> <dt>

_renderingMode * 
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

