---
title: Структура НЕВХЕАДЕР
description: Содержит число значков или компонентов курсора в группе ресурсов. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Меню структуры НЕВХЕАДЕР и другие ресурсы
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988331"
---
# <a name="newheader-structure"></a><span data-ttu-id="2b134-105">Структура НЕВХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="2b134-105">NEWHEADER structure</span></span>

<span data-ttu-id="2b134-106">Содержит число значков или компонентов курсора в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b134-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="2b134-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="2b134-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b134-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b134-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="2b134-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2b134-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b134-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2b134-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2b134-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="2b134-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2b134-112">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2b134-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b134-113">**рестипе**</span><span class="sxs-lookup"><span data-stu-id="2b134-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="2b134-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="2b134-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2b134-115">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b134-115">The resource type.</span></span> <span data-ttu-id="2b134-116">Этот элемент должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2b134-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="2b134-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2b134-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="2b134-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2b134-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="2b134-119"><dt>**RES \_ КУРСОР**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2b134-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="2b134-120">Тип ресурса курсора.</span><span class="sxs-lookup"><span data-stu-id="2b134-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="2b134-121"><dt>**RES \_ ЗНАЧОК**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2b134-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="2b134-122">Значок тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b134-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="2b134-123">**рескаунт**</span><span class="sxs-lookup"><span data-stu-id="2b134-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="2b134-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="2b134-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2b134-125">Число значков или компонентов курсора в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b134-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b134-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b134-126">Remarks</span></span>

<span data-ttu-id="2b134-127">Одна или несколько структур [**ресдир**](resdir.md) сразу же следуют структуре **невхеадер** в RES – файле.</span><span class="sxs-lookup"><span data-stu-id="2b134-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="2b134-128">Элемент **рескаунт** указывает количество структур **ресдир** .</span><span class="sxs-lookup"><span data-stu-id="2b134-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b134-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2b134-129">Requirements</span></span>



| <span data-ttu-id="2b134-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2b134-130">Requirement</span></span> | <span data-ttu-id="2b134-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2b134-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2b134-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b134-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2b134-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b134-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2b134-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b134-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2b134-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b134-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2b134-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b134-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b134-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2b134-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b134-138">**ресдир**</span><span class="sxs-lookup"><span data-stu-id="2b134-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="2b134-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2b134-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b134-140">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b134-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





