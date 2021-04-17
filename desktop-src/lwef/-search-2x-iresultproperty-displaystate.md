---
title: Свойство Дисплайстате Иресултпроперти (Вдсшаредидл. h)
description: Висабилити свойства.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- Свойства Дисплайстате устаревшие функции среды Windows
- Свойства Дисплайстате устаревшие функции среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство Дисплайстате
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85634441a38c2cb2130010c79f8ee3ebcb78a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691875"
---
# <a name="iresultpropertydisplaystate-property"></a><span data-ttu-id="71d8a-106">Иресултпроперти: свойство Исплайстате:D</span><span class="sxs-lookup"><span data-stu-id="71d8a-106">IResultProperty::DisplayState property</span></span>

> [!NOTE]
> <span data-ttu-id="71d8a-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="71d8a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="71d8a-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="71d8a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="71d8a-109">Висабилити свойства.</span><span class="sxs-lookup"><span data-stu-id="71d8a-109">Visability of the property.</span></span>

<span data-ttu-id="71d8a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="71d8a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d8a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71d8a-111">Syntax</span></span>


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a><span data-ttu-id="71d8a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="71d8a-112">Property value</span></span>

<span data-ttu-id="71d8a-113">Возвращает указатель на значение состояния отображения.</span><span class="sxs-lookup"><span data-stu-id="71d8a-113">returns a pointer to the display state value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d8a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="71d8a-114">Requirements</span></span>



| <span data-ttu-id="71d8a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="71d8a-115">Requirement</span></span> | <span data-ttu-id="71d8a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="71d8a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d8a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71d8a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71d8a-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="71d8a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="71d8a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71d8a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71d8a-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="71d8a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71d8a-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="71d8a-121">Redistributable</span></span><br/>          | <span data-ttu-id="71d8a-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="71d8a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="71d8a-123">Header</span><span class="sxs-lookup"><span data-stu-id="71d8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d8a-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d8a-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





