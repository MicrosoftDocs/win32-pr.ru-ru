---
title: Свойство DisplayName Иресулттипе (Вдсшаредидл. h)
description: Локализованное отображаемое имя типа
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701037"
---
# <a name="iresulttypedisplayname-property"></a><span data-ttu-id="89c4f-106">Иресулттипе: свойство Исплайнаме:D</span><span class="sxs-lookup"><span data-stu-id="89c4f-106">IResultType::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="89c4f-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89c4f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="89c4f-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="89c4f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="89c4f-109">Локализованное отображаемое имя типа:</span><span class="sxs-lookup"><span data-stu-id="89c4f-109">Localized display name of the type:</span></span>

<span data-ttu-id="89c4f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89c4f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c4f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89c4f-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="89c4f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89c4f-112">Property value</span></span>

<span data-ttu-id="89c4f-113">Возвращает адрес локализованного отображаемого имени для типа.</span><span class="sxs-lookup"><span data-stu-id="89c4f-113">returns the address of the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c4f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="89c4f-114">Requirements</span></span>



| <span data-ttu-id="89c4f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="89c4f-115">Requirement</span></span> | <span data-ttu-id="89c4f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="89c4f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c4f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89c4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89c4f-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="89c4f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="89c4f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89c4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89c4f-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="89c4f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="89c4f-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="89c4f-121">Redistributable</span></span><br/>          | <span data-ttu-id="89c4f-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="89c4f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="89c4f-123">Header</span><span class="sxs-lookup"><span data-stu-id="89c4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c4f-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c4f-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





