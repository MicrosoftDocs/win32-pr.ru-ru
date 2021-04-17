---
title: Структура РЕСДИР
description: Содержит сведения об отдельном значке или компоненте курсора в группе ресурсов. Для каждого компонента группы существует одна структура РЕСДИР. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Меню структуры РЕСДИР и другие ресурсы
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691791"
---
# <a name="resdir-structure"></a><span data-ttu-id="5bdf7-106">Структура РЕСДИР</span><span class="sxs-lookup"><span data-stu-id="5bdf7-106">RESDIR structure</span></span>

<span data-ttu-id="5bdf7-107">Содержит сведения об отдельном значке или компоненте курсора в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="5bdf7-108">Для каждого компонента группы существует одна структура **ресдир** .</span><span class="sxs-lookup"><span data-stu-id="5bdf7-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="5bdf7-109">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdf7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bdf7-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="5bdf7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5bdf7-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="5bdf7-112">**Значок**:</span><span class="sxs-lookup"><span data-stu-id="5bdf7-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-113">Тип: **[ **иконресдир**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-114">Ширина, высота и количество цветов указанного значка.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="5bdf7-115">**Курсор**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-116">Тип: **[ **курсордир**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-117">Ширина и высота указанного курсора.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="5bdf7-118">**Плоскост**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-119">Тип: **[ **курсордир**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-120">Число цветовых плоскостей в растровом изображении значка или курсора.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="5bdf7-121">**биткаунт**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-122">Тип: **[ **курсордир**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-123">Число битов на пиксель в битовом изображении или точечном рисунке курсора.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="5bdf7-124">**битесинрес**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-125">Тип: **[ **курсордир**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-126">Размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5bdf7-127">**иконкурсорид**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="5bdf7-128">Тип: **[ **курсордир**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5bdf7-129">Значок или курсор с уникальным порядковым идентификатором.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bdf7-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bdf7-130">Remarks</span></span>

<span data-ttu-id="5bdf7-131">Одна или несколько структур **ресдир** сразу же следуют структуре [**невхеадер**](newheader.md) в RES – файле.</span><span class="sxs-lookup"><span data-stu-id="5bdf7-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="5bdf7-132">Элемент **рескаунт** структуры **невхеадер** указывает количество структур **ресдир** .</span><span class="sxs-lookup"><span data-stu-id="5bdf7-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="5bdf7-133">Обратите внимание, что структура **ресдир** состоит из структуры [**иконресдир**](iconresdir.md) или [**курсордир**](cursordir.md) , за которой следуют элементы **плоскости**, **биткаунт**, **битесинрес** и **иконкурсорид** .</span><span class="sxs-lookup"><span data-stu-id="5bdf7-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="5bdf7-134">Если структура **ресдир** содержит сведения о курсоре, первые два **слова**, которые компилятор ресурсов записывает в ресурс [ \_ курсора RT](/windows/desktop/menurc/resource-types) , являются элементами **ксхотспот** и **ихотспот** структуры [**локалхеадер**](localheader.md) .</span><span class="sxs-lookup"><span data-stu-id="5bdf7-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bdf7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="5bdf7-135">Requirements</span></span>



| <span data-ttu-id="5bdf7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="5bdf7-136">Requirement</span></span> | <span data-ttu-id="5bdf7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5bdf7-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5bdf7-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5bdf7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5bdf7-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5bdf7-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5bdf7-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5bdf7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5bdf7-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5bdf7-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5bdf7-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bdf7-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="5bdf7-143">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5bdf7-144">**курсордир**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="5bdf7-145">**иконресдир**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="5bdf7-146">**локалхеадер**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="5bdf7-147">**невхеадер**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="5bdf7-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5bdf7-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5bdf7-149">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bdf7-149">Resources</span></span>](resources.md)
</dt> </dl>

 

