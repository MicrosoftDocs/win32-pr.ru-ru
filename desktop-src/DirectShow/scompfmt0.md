---
description: Содержит сведения о форматировании для интеллектуального повторного сжатия.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Структура SCompFmt0 (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f02c9cda80acdd42d0687502834a9b2e66f1cf773d02b88eadabdd346850061e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072708"
---
# <a name="scompfmt0-structure"></a>Структура SCompFmt0

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Содержит сведения о форматировании для интеллектуального повторного сжатия.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Члены

<dl> <dt>

**нформатид**
</dt> <dd>

Процессу должно быть равно нулю.

</dd> <dt>

**Мультимедиа**
</dt> <dd>

[**AM \_ Структура \_ типа мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) , описывающая формат сжатия.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иамтимелинеграуп:: Жетсмартрекомпрессформат**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**Иамтимелинеграуп:: Сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




