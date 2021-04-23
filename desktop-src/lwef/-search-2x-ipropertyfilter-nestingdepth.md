---
title: Свойство Нестингдепс Ипропертифилтер (Вдсшаредидл. h)
description: Отфильтровывает глубину внутри вложенного набора круглых скобок.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Свойства Нестингдепс устаревшие функции среды Windows
- Свойства Нестингдепс устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Нестингдепс
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415480"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="9995d-106">Свойство Ипропертифилтер:: Нестингдепс</span><span class="sxs-lookup"><span data-stu-id="9995d-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="9995d-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9995d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9995d-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9995d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9995d-109">Отфильтровывает глубину внутри вложенного набора круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="9995d-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="9995d-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9995d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9995d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9995d-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="9995d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9995d-112">Property value</span></span>

<span data-ttu-id="9995d-113">Задает число, указывающее глубину вложенных круглых скобок.</span><span class="sxs-lookup"><span data-stu-id="9995d-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="9995d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9995d-114">Requirements</span></span>



| <span data-ttu-id="9995d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9995d-115">Requirement</span></span> | <span data-ttu-id="9995d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9995d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9995d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9995d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9995d-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9995d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9995d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9995d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9995d-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="9995d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9995d-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9995d-121">Redistributable</span></span><br/>          | <span data-ttu-id="9995d-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9995d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9995d-123">Header</span><span class="sxs-lookup"><span data-stu-id="9995d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9995d-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9995d-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





