---
title: Интерфейс Иресултверб (Вдсшаредидл. h)
description: Предоставляет свойства команды.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Устаревшие функции среды Windows интерфейса Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691874"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="0b1d7-105">Интерфейс Иресултверб</span><span class="sxs-lookup"><span data-stu-id="0b1d7-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="0b1d7-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0b1d7-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1d7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0b1d7-108">Предоставляет свойства команды.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="0b1d7-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="0b1d7-109">Members</span></span>

<span data-ttu-id="0b1d7-110">Интерфейс **иресултверб** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0b1d7-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b1d7-111">**Иресултверб** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0b1d7-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="0b1d7-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b1d7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b1d7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0b1d7-113">Properties</span></span>

<span data-ttu-id="0b1d7-114">Интерфейс **иресултверб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="0b1d7-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="0b1d7-115">Property</span></span>                                                             | <span data-ttu-id="0b1d7-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0b1d7-116">Access type</span></span>           | <span data-ttu-id="0b1d7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0b1d7-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b1d7-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="0b1d7-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b1d7-119">Read-only</span></span><br/>  | <span data-ttu-id="0b1d7-120">Это свойство возвращает указатель на локализованное отображаемое имя для команды.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="0b1d7-121">**доит**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="0b1d7-122">Только на запись</span><span class="sxs-lookup"><span data-stu-id="0b1d7-122">Write-only</span></span><br/> | <span data-ttu-id="0b1d7-123">Выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="0b1d7-124">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="0b1d7-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b1d7-125">Read-only</span></span><br/>  | <span data-ttu-id="0b1d7-126">Это свойство возвращает значение TRUE, если команда включена.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="0b1d7-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="0b1d7-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b1d7-128">Read-only</span></span><br/>  | <span data-ttu-id="0b1d7-129">Это свойство возвращает указатель на локализованную строку справки для команды.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="0b1d7-130">**Значок**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="0b1d7-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b1d7-131">Read-only</span></span><br/>  | <span data-ttu-id="0b1d7-132">Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="0b1d7-133">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0b1d7-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="0b1d7-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0b1d7-134">Read-only</span></span><br/>  | <span data-ttu-id="0b1d7-135">Это свойство возвращает указатель на имя кононикал для команды, например Print, Open и т. д.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b1d7-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b1d7-136">Remarks</span></span>

<span data-ttu-id="0b1d7-137">Эти методы предоставляют свойства и действия, применимые к командам.</span><span class="sxs-lookup"><span data-stu-id="0b1d7-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1d7-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0b1d7-138">Requirements</span></span>



| <span data-ttu-id="0b1d7-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0b1d7-139">Requirement</span></span> | <span data-ttu-id="0b1d7-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0b1d7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1d7-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b1d7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1d7-142">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b1d7-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0b1d7-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b1d7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1d7-144">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b1d7-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b1d7-145">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0b1d7-145">Redistributable</span></span><br/>          | <span data-ttu-id="0b1d7-146">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0b1d7-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="0b1d7-147">Header</span><span class="sxs-lookup"><span data-stu-id="0b1d7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1d7-148"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1d7-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

