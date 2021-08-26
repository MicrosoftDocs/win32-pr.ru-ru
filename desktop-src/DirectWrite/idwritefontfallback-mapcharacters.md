---
title: Идвритефонтфаллбакк Мапчарактерс, метод
description: Определяет подходящий шрифт, используемый для отрисовки начального диапазона текста.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Непосредственная запись метода Мапчарактерс
- Прямая запись метода Мапчарактерс, интерфейс Идвритефонтфаллбакк
- Прямая запись интерфейса Идвритефонтфаллбакк, метод Мапчарактерс
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048794"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Метод Идвритефонтфаллбакк:: Мапчарактерс

Определяет подходящий шрифт, используемый для отрисовки начального диапазона текста.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*source* 
</dt> <dd>

Тип: **[ **идвритетекстаналисиссаурце**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

В реализации источника текста содержатся текст и языковой стандарт.

</dd> <dt>

*текстпоситион* 
</dt> <dd>

Тип: **UINT32**

Начальное расположение для анализа.

</dd> <dt>

*textLength* 
</dt> <dd>

Тип: **UINT32**

Длина анализируемого текста.

</dd> <dt>

*басефонтколлектион* \[ в необязательное\]
</dt> <dd>

Тип: **[ **идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

Используемая коллекция шрифтов по умолчанию.

</dd> <dt>

*басефамилинаме* \[ в необязательное\]
</dt> <dd>

Тип: **const WCHAR \_ t \***

Имя семейства базовых шрифтов. Если передать значение null, для семейства не будет выполняться никаких соответствий.

</dd> <dt>

*басевеигхт* 
</dt> <dd>

Тип: **[ **\_ \_ плотность шрифта дврите**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Требуемый вес.

</dd> <dt>

*басестиле* 
</dt> <dd>

Тип: Дврите начертание **[ **\_ шрифта \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Нужный стиль.

</dd> <dt>

*басестретч* 
</dt> <dd>

Тип: **[ **дврите \_ Font \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Требуемое растяжение.

</dd> <dt>

*маппедленгс* \[ заполняет\]
</dt> <dd>

Тип: **UINT32 \***

Длина текста, сопоставленного с сопоставленным шрифтом. Оно всегда будет меньше или равно длине текста и больше нуля (если длина текста не равна нулю), поэтому вызывающий объект перемещает по крайней мере один символ.

</dd> <dt>

*маппедфонт* \[ заполняет\]
</dt> <dd>

Тип: **[ **идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Шрифт, который должен использоваться для отрисовки первых *маппедленгс* символов текста. Если он возвращает значение NULL, это означает, что ни один из шрифтов не может визуализировать текст, а *маппедленгс* — число пропускаемых символов (отображается с отсутствующим глифом).

</dd> <dt>

*масштаб* \[ заполняет\]
</dt> <dd>

Тип: **float \***

Коэффициент масштабирования для умножения размера em возвращаемого шрифта на.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                 |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**идвритефонтфаллбакк**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

