---
title: Интерфейс Ипропертифилтер (Вдсшаредидл. h)
description: Отображает свойства, используемые для фильтрации запроса.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Устаревшие функции среды Windows интерфейса Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534697"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="f1b97-105">Интерфейс Ипропертифилтер</span><span class="sxs-lookup"><span data-stu-id="f1b97-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="f1b97-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f1b97-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f1b97-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f1b97-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f1b97-108">Отображает свойства, используемые для фильтрации запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b97-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="f1b97-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="f1b97-109">Members</span></span>

<span data-ttu-id="f1b97-110">Интерфейс **ипропертифилтер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f1b97-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f1b97-111">**Ипропертифилтер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f1b97-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="f1b97-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1b97-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1b97-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1b97-113">Properties</span></span>

<span data-ttu-id="f1b97-114">Интерфейс **ипропертифилтер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f1b97-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="f1b97-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="f1b97-115">Property</span></span>                                                                                      | <span data-ttu-id="f1b97-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f1b97-116">Access type</span></span>           | <span data-ttu-id="f1b97-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f1b97-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="f1b97-118">**Ипропертифилтер:: Индексколумн**</span><span class="sxs-lookup"><span data-stu-id="f1b97-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="f1b97-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f1b97-119">Read/write</span></span><br/> | <span data-ttu-id="f1b97-120">Имя индексируемого столбца свойства, по которому производится фильтрация.</span><span class="sxs-lookup"><span data-stu-id="f1b97-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="f1b97-121">**Ипропертифилтер:: Логикоператор**</span><span class="sxs-lookup"><span data-stu-id="f1b97-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="f1b97-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f1b97-122">Read/write</span></span><br/> | <span data-ttu-id="f1b97-123">Логический оператор, используемый при применении фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1b97-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="f1b97-124">**Ипропертифилтер:: Нестингдепс**</span><span class="sxs-lookup"><span data-stu-id="f1b97-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="f1b97-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f1b97-125">Read/write</span></span><br/> | <span data-ttu-id="f1b97-126">Отфильтровывает глубину внутри вложенного набора круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="f1b97-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="f1b97-127">**Ипропертифилтер:: Text**</span><span class="sxs-lookup"><span data-stu-id="f1b97-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="f1b97-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f1b97-128">Read/write</span></span><br/> | <span data-ttu-id="f1b97-129">Текст фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1b97-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="f1b97-130">**Ипропертифилтер:: UID**</span><span class="sxs-lookup"><span data-stu-id="f1b97-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="f1b97-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f1b97-131">Read/write</span></span><br/> | <span data-ttu-id="f1b97-132">UID свойства, по которому необходимо выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f1b97-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="f1b97-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1b97-133">Remarks</span></span>

<span data-ttu-id="f1b97-134">Эти свойства используются для фильтрации запроса.</span><span class="sxs-lookup"><span data-stu-id="f1b97-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b97-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f1b97-135">Requirements</span></span>



| <span data-ttu-id="f1b97-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f1b97-136">Requirement</span></span> | <span data-ttu-id="f1b97-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f1b97-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b97-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1b97-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b97-139">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1b97-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f1b97-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1b97-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b97-141">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1b97-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1b97-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f1b97-142">Redistributable</span></span><br/>          | <span data-ttu-id="f1b97-143">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="f1b97-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="f1b97-144">Header</span><span class="sxs-lookup"><span data-stu-id="f1b97-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b97-145"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b97-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

