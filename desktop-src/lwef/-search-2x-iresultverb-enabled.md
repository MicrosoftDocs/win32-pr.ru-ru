---
title: Свойство Иресултверб Enabled (Вдсшаредидл. h)
description: Это свойство возвращает значение TRUE, если команда включена.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Включенное свойство "устаревшие функции среды Windows"
- Включенное свойство. устаревшие функции среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство Enabled
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988927"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="33a1e-106">Свойство Иресултверб:: Enabled</span><span class="sxs-lookup"><span data-stu-id="33a1e-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="33a1e-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="33a1e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="33a1e-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="33a1e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="33a1e-109">Это свойство возвращает значение TRUE, если команда включена.</span><span class="sxs-lookup"><span data-stu-id="33a1e-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="33a1e-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33a1e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a1e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33a1e-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="33a1e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="33a1e-112">Property value</span></span>

<span data-ttu-id="33a1e-113">Это свойство возвращает значение true, если команда включена, или значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="33a1e-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a1e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="33a1e-114">Requirements</span></span>



| <span data-ttu-id="33a1e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="33a1e-115">Requirement</span></span> | <span data-ttu-id="33a1e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33a1e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a1e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33a1e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33a1e-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33a1e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="33a1e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33a1e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33a1e-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="33a1e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="33a1e-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="33a1e-121">Redistributable</span></span><br/>          | <span data-ttu-id="33a1e-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="33a1e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="33a1e-123">Header</span><span class="sxs-lookup"><span data-stu-id="33a1e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a1e-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a1e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





