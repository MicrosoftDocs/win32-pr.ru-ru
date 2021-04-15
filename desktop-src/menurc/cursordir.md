---
title: Структура КУРСОРДИР
description: Содержит размеры отдельного изображения курсора в группе ресурсов. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Меню структуры КУРСОРДИР и другие ресурсы
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416001"
---
# <a name="cursordir-structure"></a><span data-ttu-id="5b461-105">Структура КУРСОРДИР</span><span class="sxs-lookup"><span data-stu-id="5b461-105">CURSORDIR structure</span></span>

<span data-ttu-id="5b461-106">Содержит размеры отдельного изображения курсора в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b461-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="5b461-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="5b461-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b461-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b461-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="5b461-109">Члены</span><span class="sxs-lookup"><span data-stu-id="5b461-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b461-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="5b461-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="5b461-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5b461-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5b461-112">Ширина курсора в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5b461-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="5b461-113">Допустимые значения: 16, 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="5b461-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="5b461-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="5b461-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="5b461-115">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="5b461-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="5b461-116">Высота курсора в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5b461-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="5b461-117">Допустимые значения: 16, 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="5b461-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b461-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b461-118">Remarks</span></span>

<span data-ttu-id="5b461-119">Структура **курсордир** передается в структуру [**ресдир**](resdir.md) , если структура **ресдир** описывает курсор.</span><span class="sxs-lookup"><span data-stu-id="5b461-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b461-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5b461-120">Requirements</span></span>



| <span data-ttu-id="5b461-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5b461-121">Requirement</span></span> | <span data-ttu-id="5b461-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5b461-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5b461-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b461-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b461-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b461-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5b461-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b461-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b461-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b461-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5b461-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b461-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b461-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5b461-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b461-129">**ресдир**</span><span class="sxs-lookup"><span data-stu-id="5b461-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="5b461-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5b461-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b461-131">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b461-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





