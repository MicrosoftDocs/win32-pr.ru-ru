---
title: Свойство UID Ипропертифилтер (Вдсшаредидл. h)
description: Идентификатор UID для свойства, по которому производится фильтрация.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Свойства UID устаревшие функции среды Windows
- Свойство UID устаревшие компоненты среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340900"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="7c6a2-106">Свойство Ипропертифилтер:: UID</span><span class="sxs-lookup"><span data-stu-id="7c6a2-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="7c6a2-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7c6a2-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6a2-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7c6a2-109">Идентификатор UID для свойства, по которому производится фильтрация.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-109">UID for the property to filter by.</span></span>

<span data-ttu-id="7c6a2-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6a2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c6a2-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="7c6a2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7c6a2-112">Property value</span></span>

<span data-ttu-id="7c6a2-113">Задает свойство UID.</span><span class="sxs-lookup"><span data-stu-id="7c6a2-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6a2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7c6a2-114">Requirements</span></span>



| <span data-ttu-id="7c6a2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7c6a2-115">Requirement</span></span> | <span data-ttu-id="7c6a2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c6a2-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6a2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c6a2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6a2-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c6a2-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7c6a2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c6a2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6a2-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c6a2-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c6a2-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7c6a2-121">Redistributable</span></span><br/>          | <span data-ttu-id="7c6a2-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7c6a2-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7c6a2-123">Header</span><span class="sxs-lookup"><span data-stu-id="7c6a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c6a2-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6a2-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





