---
title: Свойство UID Иресулттипе (Вдсшаредидл. h)
description: Это свойство содержит уникальный идентификатор для типа.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Свойства UID устаревшие функции среды Windows
- Свойство UID устаревшие компоненты среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137647"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="a743a-106">Свойство Иресулттипе:: UID</span><span class="sxs-lookup"><span data-stu-id="a743a-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="a743a-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a743a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a743a-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a743a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a743a-109">Это свойство содержит уникальный идентификатор для типа.</span><span class="sxs-lookup"><span data-stu-id="a743a-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="a743a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a743a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a743a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a743a-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="a743a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a743a-112">Property value</span></span>

<span data-ttu-id="a743a-113">адрес расположения, содержащего идентификатор UID.</span><span class="sxs-lookup"><span data-stu-id="a743a-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="a743a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a743a-114">Requirements</span></span>



| <span data-ttu-id="a743a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a743a-115">Requirement</span></span> | <span data-ttu-id="a743a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a743a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a743a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a743a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a743a-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a743a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a743a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a743a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a743a-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="a743a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a743a-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a743a-121">Redistributable</span></span><br/>          | <span data-ttu-id="a743a-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="a743a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="a743a-123">Header</span><span class="sxs-lookup"><span data-stu-id="a743a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a743a-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a743a-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





