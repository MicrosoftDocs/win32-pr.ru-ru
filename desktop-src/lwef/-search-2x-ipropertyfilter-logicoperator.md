---
title: Свойство Логикоператор Ипропертифилтер (Вдсшаредидл. h)
description: Логический оператор, используемый при применении фильтра.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Свойства Логикоператор устаревшие функции среды Windows
- Свойства Логикоператор устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Логикоператор
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493065"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="e4b51-106">Свойство Ипропертифилтер:: Логикоператор</span><span class="sxs-lookup"><span data-stu-id="e4b51-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="e4b51-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e4b51-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e4b51-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b51-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e4b51-109">Логический оператор, используемый при применении фильтра.</span><span class="sxs-lookup"><span data-stu-id="e4b51-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="e4b51-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e4b51-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b51-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b51-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="e4b51-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e4b51-112">Property value</span></span>

<span data-ttu-id="e4b51-113">Задает тип логического оператора.</span><span class="sxs-lookup"><span data-stu-id="e4b51-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b51-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b51-114">Requirements</span></span>



| <span data-ttu-id="e4b51-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b51-115">Requirement</span></span> | <span data-ttu-id="e4b51-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b51-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b51-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b51-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4b51-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e4b51-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b51-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4b51-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4b51-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e4b51-121">Redistributable</span></span><br/>          | <span data-ttu-id="e4b51-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e4b51-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e4b51-123">Header</span><span class="sxs-lookup"><span data-stu-id="e4b51-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b51-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b51-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





