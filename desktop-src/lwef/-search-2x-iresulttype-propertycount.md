---
title: Свойство Пропертикаунт Иресулттипе (Вдсшаредидл. h)
description: Это свойство содержит количество свойств, предоставляемых типом.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Свойства Пропертикаунт устаревшие функции среды Windows
- Свойства Пропертикаунт устаревшие функции среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство Пропертикаунт
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533776"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="d9af8-106">Иресулттипе: свойство Ропертикаунт:P</span><span class="sxs-lookup"><span data-stu-id="d9af8-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="d9af8-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d9af8-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d9af8-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d9af8-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d9af8-109">Это свойство содержит количество свойств, предоставляемых типом.</span><span class="sxs-lookup"><span data-stu-id="d9af8-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="d9af8-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d9af8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9af8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9af8-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="d9af8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d9af8-112">Property value</span></span>

<span data-ttu-id="d9af8-113">Возвращает адрес числа предоставленных свойств.</span><span class="sxs-lookup"><span data-stu-id="d9af8-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9af8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d9af8-114">Requirements</span></span>



| <span data-ttu-id="d9af8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d9af8-115">Requirement</span></span> | <span data-ttu-id="d9af8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d9af8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9af8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9af8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d9af8-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9af8-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d9af8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9af8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d9af8-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9af8-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9af8-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d9af8-121">Redistributable</span></span><br/>          | <span data-ttu-id="d9af8-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d9af8-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d9af8-123">Header</span><span class="sxs-lookup"><span data-stu-id="d9af8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9af8-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9af8-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





