---
title: Интерфейс Иресулттипе (Вдсшаредидл. h)
description: Предоставляет сведения о типе свойства.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Устаревшие функции среды Windows интерфейса Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490020"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="a8d82-105">Интерфейс Иресулттипе</span><span class="sxs-lookup"><span data-stu-id="a8d82-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="a8d82-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8d82-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a8d82-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d82-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a8d82-108">Предоставляет сведения о типе свойства.</span><span class="sxs-lookup"><span data-stu-id="a8d82-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="a8d82-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="a8d82-109">Members</span></span>

<span data-ttu-id="a8d82-110">Интерфейс **иресулттипе** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a8d82-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8d82-111">**Иресулттипе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8d82-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="a8d82-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8d82-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8d82-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8d82-113">Properties</span></span>

<span data-ttu-id="a8d82-114">Интерфейс **иресулттипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8d82-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="a8d82-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="a8d82-115">Property</span></span>                                                                 | <span data-ttu-id="a8d82-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a8d82-116">Access type</span></span>           | <span data-ttu-id="a8d82-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a8d82-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8d82-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a8d82-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="a8d82-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8d82-119">Read-only</span></span><br/>  | <span data-ttu-id="a8d82-120">Локализованное отображаемое имя типа:</span><span class="sxs-lookup"><span data-stu-id="a8d82-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="a8d82-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="a8d82-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="a8d82-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a8d82-122">Read/write</span></span><br/> | <span data-ttu-id="a8d82-123">Это свойство содержит указанные сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="a8d82-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="a8d82-124">**прецеиведтипе**</span><span class="sxs-lookup"><span data-stu-id="a8d82-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="a8d82-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8d82-125">Read-only</span></span><br/>  | <span data-ttu-id="a8d82-126">Это свойство содержит строку, используемую для задания типа в индексе.</span><span class="sxs-lookup"><span data-stu-id="a8d82-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="a8d82-127">**пропертикаунт**</span><span class="sxs-lookup"><span data-stu-id="a8d82-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="a8d82-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8d82-128">Read-only</span></span><br/>  | <span data-ttu-id="a8d82-129">Это свойство содержит количество свойств, предоставляемых типом.</span><span class="sxs-lookup"><span data-stu-id="a8d82-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="a8d82-130">**ИД пользователя**</span><span class="sxs-lookup"><span data-stu-id="a8d82-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="a8d82-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8d82-131">Read-only</span></span><br/>  | <span data-ttu-id="a8d82-132">Это свойство содержит уникальный идентификатор для типа.</span><span class="sxs-lookup"><span data-stu-id="a8d82-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="a8d82-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8d82-133">Remarks</span></span>

<span data-ttu-id="a8d82-134">Эти методы предоставляют типы возвращаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="a8d82-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d82-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a8d82-135">Requirements</span></span>



| <span data-ttu-id="a8d82-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a8d82-136">Requirement</span></span> | <span data-ttu-id="a8d82-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a8d82-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d82-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8d82-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d82-139">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8d82-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a8d82-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8d82-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d82-141">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8d82-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a8d82-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a8d82-142">Redistributable</span></span><br/>          | <span data-ttu-id="a8d82-143">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a8d82-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="a8d82-144">Header</span><span class="sxs-lookup"><span data-stu-id="a8d82-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d82-145"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d82-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

