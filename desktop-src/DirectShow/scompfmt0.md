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
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675503"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иамтимелинеграуп:: Жетсмартрекомпрессформат**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**Иамтимелинеграуп:: Сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




