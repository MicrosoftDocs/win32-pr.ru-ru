---
title: Свойство имени Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на имя кононикал для команды, например Print, Open и т. д.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Свойство Name устаревшие функции среды Windows
- Свойство Name устаревшие компоненты среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988250"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="d17c0-106">Свойство Иресултверб:: Name</span><span class="sxs-lookup"><span data-stu-id="d17c0-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="d17c0-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d17c0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d17c0-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d17c0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d17c0-109">Это свойство возвращает указатель на имя кононикал для команды, например Print, Open и т. д.</span><span class="sxs-lookup"><span data-stu-id="d17c0-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="d17c0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d17c0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17c0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d17c0-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="d17c0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d17c0-112">Property value</span></span>

<span data-ttu-id="d17c0-113">Name — это указатель на имя кононикал для команды.</span><span class="sxs-lookup"><span data-stu-id="d17c0-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="d17c0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d17c0-114">Requirements</span></span>



| <span data-ttu-id="d17c0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d17c0-115">Requirement</span></span> | <span data-ttu-id="d17c0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d17c0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17c0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d17c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d17c0-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d17c0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d17c0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d17c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d17c0-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="d17c0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d17c0-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d17c0-121">Redistributable</span></span><br/>          | <span data-ttu-id="d17c0-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d17c0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d17c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="d17c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d17c0-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d17c0-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





