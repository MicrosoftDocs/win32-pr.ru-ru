---
title: Свойство DisplayName Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на локализованное отображаемое имя для команды.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071477"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="c51cc-106">Иресултверб: свойство Исплайнаме:D</span><span class="sxs-lookup"><span data-stu-id="c51cc-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="c51cc-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c51cc-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c51cc-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c51cc-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c51cc-109">Это свойство возвращает указатель на локализованное отображаемое имя для команды.</span><span class="sxs-lookup"><span data-stu-id="c51cc-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="c51cc-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c51cc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51cc-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c51cc-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="c51cc-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c51cc-112">Property value</span></span>

<span data-ttu-id="c51cc-113">Это свойство возвращает указатель на локализованное отображаемое имя для команды.</span><span class="sxs-lookup"><span data-stu-id="c51cc-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51cc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c51cc-114">Requirements</span></span>



| <span data-ttu-id="c51cc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c51cc-115">Requirement</span></span> | <span data-ttu-id="c51cc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c51cc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51cc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c51cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c51cc-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c51cc-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c51cc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c51cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c51cc-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="c51cc-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c51cc-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c51cc-121">Redistributable</span></span><br/>          | <span data-ttu-id="c51cc-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c51cc-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c51cc-123">Header</span><span class="sxs-lookup"><span data-stu-id="c51cc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c51cc-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51cc-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





