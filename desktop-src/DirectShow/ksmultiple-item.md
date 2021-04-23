---
description: '\_Структура элемента ксмултипле описывает размер и число свойств переменной длины в ПИН-кодах в режиме ядра.'
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Структура KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675927"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="32c0c-103">\_Структура элемента ксмултипле</span><span class="sxs-lookup"><span data-stu-id="32c0c-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="32c0c-104">`KSMULTIPLE_ITEM`Структура описывает размер и число свойств переменной длины ПИН-кодов в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="32c0c-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32c0c-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="32c0c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="32c0c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32c0c-107">**Размер**</span><span class="sxs-lookup"><span data-stu-id="32c0c-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="32c0c-108">Размер возвращенного блока памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="32c0c-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="32c0c-109">Размер включает структуру **\_ элемента ксмултипле** и элементы, которые следуют за ней.</span><span class="sxs-lookup"><span data-stu-id="32c0c-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="32c0c-110">**Количество**</span><span class="sxs-lookup"><span data-stu-id="32c0c-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="32c0c-111">Указывает общее число элементов, которые следуют за этой структурой.</span><span class="sxs-lookup"><span data-stu-id="32c0c-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32c0c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="32c0c-112">Requirements</span></span>



| <span data-ttu-id="32c0c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="32c0c-113">Requirement</span></span> | <span data-ttu-id="32c0c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="32c0c-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="32c0c-115">Header</span><span class="sxs-lookup"><span data-stu-id="32c0c-115">Header</span></span><br/> | <dl> <span data-ttu-id="32c0c-116"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c0c-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c0c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32c0c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c0c-118">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="32c0c-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="32c0c-119">**Икспин:: Кскуеримедиумс**</span><span class="sxs-lookup"><span data-stu-id="32c0c-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="32c0c-120">**регпинмедиум**</span><span class="sxs-lookup"><span data-stu-id="32c0c-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




