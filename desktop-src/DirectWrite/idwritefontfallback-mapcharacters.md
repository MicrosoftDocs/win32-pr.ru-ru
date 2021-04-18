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
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340835"
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

Тип: **[**идвритетекстаналисиссаурце**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

В реализации источника текста содержатся текст и языковой стандарт.

</dd> <dt>

_textPosition * 
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

Тип: **[**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Используемая коллекция шрифтов по умолчанию.

</dd> <dt>

_baseFamilyName * \[ в, необязательно\]
</dt> <dd>

Тип: **const WCHAR \_ t \** _

Имя семейства базовых шрифтов. Если передать значение null, для семейства не будет выполняться никаких соответствий.

</dd> <dt>

_baseWeight * 
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

Тип: **UINT32 \** _

Длина текста, сопоставленного с сопоставленным шрифтом. Оно всегда будет меньше или равно длине текста и больше нуля (если длина текста не равна нулю), поэтому вызывающий объект перемещает по крайней мере один символ.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Тип: **[ **идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Шрифт, который должен использоваться для отрисовки первых *маппедленгс* символов текста. Если он возвращает значение NULL, это означает, что ни один из шрифтов не может визуализировать текст, а *маппедленгс* — число пропускаемых символов (отображается с отсутствующим глифом).

</dd> <dt>

*масштаб* \[ заполняет\]
</dt> <dd>

Тип: **float \** _

Коэффициент масштабирования для умножения размера em возвращаемого шрифта на.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                 |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идвритефонтфаллбакк**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

