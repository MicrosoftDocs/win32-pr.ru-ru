---
title: Свойство HelpText Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на локализованную строку справки для команды.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Свойства HelpText устаревшие функции среды Windows
- Свойства HelpText устаревшие функции среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство HelpText
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801925"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="0e9c3-106">Свойство Иресултверб:: HelpText</span><span class="sxs-lookup"><span data-stu-id="0e9c3-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="0e9c3-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0e9c3-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="0e9c3-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0e9c3-109">Это свойство возвращает указатель на локализованную строку справки для команды.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="0e9c3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9c3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e9c3-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="0e9c3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0e9c3-112">Property value</span></span>

<span data-ttu-id="0e9c3-113">Значение этого свойства является указателем на локализованную строку справки для этой команды.</span><span class="sxs-lookup"><span data-stu-id="0e9c3-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9c3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0e9c3-114">Requirements</span></span>



| <span data-ttu-id="0e9c3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0e9c3-115">Requirement</span></span> | <span data-ttu-id="0e9c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0e9c3-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9c3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e9c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9c3-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9c3-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0e9c3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e9c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9c3-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9c3-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e9c3-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0e9c3-121">Redistributable</span></span><br/>          | <span data-ttu-id="0e9c3-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="0e9c3-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="0e9c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="0e9c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9c3-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9c3-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





