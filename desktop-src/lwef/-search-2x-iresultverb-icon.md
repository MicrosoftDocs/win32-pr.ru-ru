---
title: Свойство Icon Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Свойство Icon устаревшие функции среды Windows
- Свойство Icon устаревшие функции среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491559"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="d3534-106">Свойство Иресултверб:: Icon</span><span class="sxs-lookup"><span data-stu-id="d3534-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="d3534-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3534-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d3534-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d3534-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d3534-109">Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.</span><span class="sxs-lookup"><span data-stu-id="d3534-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="d3534-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3534-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3534-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3534-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="d3534-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d3534-112">Property value</span></span>

<span data-ttu-id="d3534-113">Хикон — это указатель на маркер необязательного значка ассокуатед с командой.</span><span class="sxs-lookup"><span data-stu-id="d3534-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3534-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d3534-114">Requirements</span></span>



| <span data-ttu-id="d3534-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d3534-115">Requirement</span></span> | <span data-ttu-id="d3534-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d3534-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3534-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3534-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3534-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3534-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d3534-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3534-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3534-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3534-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3534-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d3534-121">Redistributable</span></span><br/>          | <span data-ttu-id="d3534-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d3534-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d3534-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3534-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3534-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3534-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





