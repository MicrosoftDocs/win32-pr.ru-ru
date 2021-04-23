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
# <a name="scompfmt0-structure"></a><span data-ttu-id="29d9c-103">Структура SCompFmt0</span><span class="sxs-lookup"><span data-stu-id="29d9c-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="29d9c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="29d9c-104">\[Deprecated.</span></span> <span data-ttu-id="29d9c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29d9c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="29d9c-106">Содержит сведения о форматировании для интеллектуального повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="29d9c-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29d9c-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="29d9c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="29d9c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="29d9c-109">**нформатид**</span><span class="sxs-lookup"><span data-stu-id="29d9c-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="29d9c-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="29d9c-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="29d9c-111">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="29d9c-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="29d9c-112">[**AM \_ Структура \_ типа мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) , описывающая формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="29d9c-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29d9c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="29d9c-113">Requirements</span></span>



| <span data-ttu-id="29d9c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="29d9c-114">Requirement</span></span> | <span data-ttu-id="29d9c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="29d9c-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29d9c-116">Header</span><span class="sxs-lookup"><span data-stu-id="29d9c-116">Header</span></span><br/> | <dl> <span data-ttu-id="29d9c-117"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d9c-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d9c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29d9c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d9c-119">**Иамтимелинеграуп:: Жетсмартрекомпрессформат**</span><span class="sxs-lookup"><span data-stu-id="29d9c-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="29d9c-120">**Иамтимелинеграуп:: Сетсмартрекомпрессформат**</span><span class="sxs-lookup"><span data-stu-id="29d9c-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




