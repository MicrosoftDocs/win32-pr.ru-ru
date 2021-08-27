---
description: Перечисление перечислений \_ страниц мксдк S0 \_ \_ используется для указания типов ресурсов, которые могут быть связаны со страницами в документах XPS и могут обрабатываться или передаваться необработанным конвертером документов XPS (мксдк) в выходные данные.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Перечисление MXDC_S0_PAGE_ENUMS (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471319"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Перечисление перечислений \_ страниц мксдк S0 \_ \_

Перечисление перечислений **\_ \_ страниц \_ мксдк S0** используется для указания типов ресурсов, которые могут быть связаны со страницами в документах XPS и могут обрабатываться или передаваться необработанным конвертером документов XPS (мксдк) в выходные данные.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**МКСДК \_ Resource \_ TTF**
</dt> <dd>

Шрифт TrueType или OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**МКСДК \_ ресурс \_ JPEG**
</dt> <dd>

Изображение JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**МКСДК \_ ресурс \_ PNG**
</dt> <dd>

Изображение PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**МКСДК \_ ресурсов \_ TIFF**
</dt> <dd>

Изображение TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_формате WDP ресурсов \_ мксдк**
</dt> <dd>

Windows Изображение фотографии мультимедиа.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_словарь ресурсов \_ мксдк**
</dt> <dd>

Удаленный словарь ресурсов, который должен быть передан в выходные данные МКСДК, не обрабатываются.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ профиль ICC ресурса \_ мксдк**
</dt> <dd>

Профиль ICC, который должен быть передан в выходные данные МКСДК, не обрабатываются.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ эскиз JPEG ресурса \_ мксдк**
</dt> <dd>

Эскиз JPEG, который должен быть передан в выходные данные МКСДК в необработанном виде.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_эскиз ресурса \_ PNG \_ мксдк**
</dt> <dd>

Эскиз PNG, который должен быть передан в выходные данные МКСДК в необработанном виде.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**\_ \_ максимальный размер ресурса мксдк**
</dt> <dd>

Максимальное число ресурсов для проверки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление в основном используется в качестве члена **двресаурцетипе** структуры [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



 

 




