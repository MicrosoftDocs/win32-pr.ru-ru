---
title: Свойство Иресулттипе-Property (Вдсшаредидл. h)
description: Это свойство содержит указанные сведения о свойстве.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Свойства свойств. устаревшие функции среды Windows
- Свойство свойства Property устаревшие функции среды Windows, интерфейс Иресулттипе
- Устаревшие функции среды Windows интерфейса Иресулттипе, свойство Property
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891726"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="8b652-106">Свойство Иресулттипе:: Property</span><span class="sxs-lookup"><span data-stu-id="8b652-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="8b652-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8b652-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8b652-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8b652-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8b652-109">Это свойство содержит указанные сведения о свойстве.</span><span class="sxs-lookup"><span data-stu-id="8b652-109">This property contains specified property information.</span></span>

<span data-ttu-id="8b652-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8b652-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b652-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b652-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="8b652-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8b652-112">Property value</span></span>

<span data-ttu-id="8b652-113">Задает адрес указанных сведений о свойстве.</span><span class="sxs-lookup"><span data-stu-id="8b652-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b652-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8b652-114">Requirements</span></span>



| <span data-ttu-id="8b652-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8b652-115">Requirement</span></span> | <span data-ttu-id="8b652-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b652-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b652-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b652-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b652-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b652-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8b652-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b652-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b652-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b652-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b652-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8b652-121">Redistributable</span></span><br/>          | <span data-ttu-id="8b652-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8b652-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="8b652-123">Header</span><span class="sxs-lookup"><span data-stu-id="8b652-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b652-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b652-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





