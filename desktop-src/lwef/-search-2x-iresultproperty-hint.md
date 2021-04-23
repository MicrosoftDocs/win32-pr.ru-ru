---
title: Свойство подсказки Иресултпроперти (Вдсшаредидл. h)
description: Специальное значение, используемое для облегчения извлечения данных.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Свойство подсказки устаревшие функции среды Windows
- Свойство подсказки устаревшие функции среды Windows, интерфейс Иресултпроперти
- Устаревшие функции среды Windows интерфейса Иресултпроперти, свойство указания
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691798"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="fcb63-106">Иресултпроперти:: Указание свойства</span><span class="sxs-lookup"><span data-stu-id="fcb63-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="fcb63-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fcb63-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="fcb63-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb63-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="fcb63-109">Специальное значение, используемое для облегчения извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="fcb63-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="fcb63-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fcb63-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb63-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcb63-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="fcb63-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fcb63-112">Property value</span></span>

<span data-ttu-id="fcb63-113">Возвращает указатель на подсказку.</span><span class="sxs-lookup"><span data-stu-id="fcb63-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb63-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fcb63-114">Requirements</span></span>



| <span data-ttu-id="fcb63-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fcb63-115">Requirement</span></span> | <span data-ttu-id="fcb63-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb63-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb63-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcb63-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb63-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcb63-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fcb63-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcb63-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb63-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcb63-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fcb63-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="fcb63-121">Redistributable</span></span><br/>          | <span data-ttu-id="fcb63-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="fcb63-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="fcb63-123">Header</span><span class="sxs-lookup"><span data-stu-id="fcb63-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcb63-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcb63-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





