---
title: Свойство UID Иресултпроперти (Вдсшаредидл. h)
description: Уникальный идентификатор свойства.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Свойства UID устаревшие функции среды Windows
- Свойство UID устаревшие компоненты среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071479"
---
# <a name="iresultpropertyuid-property"></a><span data-ttu-id="e814f-106">Свойство Иресултпроперти:: UID</span><span class="sxs-lookup"><span data-stu-id="e814f-106">IResultProperty::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="e814f-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e814f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e814f-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="e814f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e814f-109">Уникальный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="e814f-109">Unique identifier for the property.</span></span>

<span data-ttu-id="e814f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e814f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e814f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e814f-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="e814f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e814f-112">Property value</span></span>

<span data-ttu-id="e814f-113">Возвращает указатель на уникальный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="e814f-113">returns a pointer to the unique property identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e814f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e814f-114">Requirements</span></span>



| <span data-ttu-id="e814f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e814f-115">Requirement</span></span> | <span data-ttu-id="e814f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e814f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e814f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e814f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e814f-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e814f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e814f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e814f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e814f-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="e814f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e814f-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e814f-121">Redistributable</span></span><br/>          | <span data-ttu-id="e814f-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e814f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e814f-123">Header</span><span class="sxs-lookup"><span data-stu-id="e814f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e814f-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e814f-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





