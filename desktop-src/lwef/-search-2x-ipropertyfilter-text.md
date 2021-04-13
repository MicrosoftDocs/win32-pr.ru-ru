---
title: Свойство Text Ипропертифилтер (Вдсшаредидл. h)
description: Текст фильтра.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Свойства текста устаревшие функции среды Windows
- Свойство текста устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534700"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="773a5-106">Свойство Ипропертифилтер:: Text</span><span class="sxs-lookup"><span data-stu-id="773a5-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="773a5-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="773a5-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="773a5-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="773a5-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="773a5-109">Текст фильтра.</span><span class="sxs-lookup"><span data-stu-id="773a5-109">Text of the filter.</span></span>

<span data-ttu-id="773a5-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="773a5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="773a5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="773a5-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="773a5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="773a5-112">Property value</span></span>

<span data-ttu-id="773a5-113">Задает текст фильтра.</span><span class="sxs-lookup"><span data-stu-id="773a5-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="773a5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="773a5-114">Requirements</span></span>



| <span data-ttu-id="773a5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="773a5-115">Requirement</span></span> | <span data-ttu-id="773a5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="773a5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="773a5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="773a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="773a5-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="773a5-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="773a5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="773a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="773a5-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="773a5-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="773a5-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="773a5-121">Redistributable</span></span><br/>          | <span data-ttu-id="773a5-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="773a5-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="773a5-123">Header</span><span class="sxs-lookup"><span data-stu-id="773a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="773a5-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="773a5-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





