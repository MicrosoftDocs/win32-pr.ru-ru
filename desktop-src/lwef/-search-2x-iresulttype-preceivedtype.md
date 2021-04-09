---
title: Свойство Прецеиведтипе Иресулттипе (Вдсшаредидл. h)
description: Это свойство содержит строку, используемую для задания типа в индексе.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Свойства Прецеиведтипе устаревшие функции среды Windows
- Свойства Прецеиведтипе устаревшие функции среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство Прецеиведтипе
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891725"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="75c1c-106">Иресулттипе: свойство Рецеиведтипе:P</span><span class="sxs-lookup"><span data-stu-id="75c1c-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="75c1c-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="75c1c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="75c1c-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="75c1c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="75c1c-109">Это свойство содержит строку, используемую для задания типа в индексе.</span><span class="sxs-lookup"><span data-stu-id="75c1c-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="75c1c-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="75c1c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c1c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75c1c-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="75c1c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="75c1c-112">Property value</span></span>

<span data-ttu-id="75c1c-113">Возвращает адрес строки, идентифинт тип в индексе.</span><span class="sxs-lookup"><span data-stu-id="75c1c-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c1c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="75c1c-114">Requirements</span></span>



| <span data-ttu-id="75c1c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="75c1c-115">Requirement</span></span> | <span data-ttu-id="75c1c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="75c1c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c1c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75c1c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75c1c-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="75c1c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="75c1c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75c1c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75c1c-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="75c1c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="75c1c-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="75c1c-121">Redistributable</span></span><br/>          | <span data-ttu-id="75c1c-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="75c1c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="75c1c-123">Header</span><span class="sxs-lookup"><span data-stu-id="75c1c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75c1c-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c1c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





