---
title: Структура Мрмресаурцеиндексерхандле (Мрмресаурцеиндексер. h)
description: Представляет непрозрачный маркер для объекта индексатора ресурса. Этот маркер управляется операционной системой. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Меню структуры Мрмресаурцеиндексерхандле и другие ресурсы
- Меню указателя структуры Пмрмресаурцеиндексерхандле и другие ресурсы
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416125"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="8162b-107">Структура Мрмресаурцеиндексерхандле</span><span class="sxs-lookup"><span data-stu-id="8162b-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="8162b-108">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8162b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8162b-109">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8162b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8162b-110">Представляет непрозрачный маркер для объекта индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="8162b-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="8162b-111">Этот маркер управляется операционной системой.</span><span class="sxs-lookup"><span data-stu-id="8162b-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="8162b-112">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8162b-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8162b-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8162b-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="8162b-114">Члены</span><span class="sxs-lookup"><span data-stu-id="8162b-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="8162b-115">**справиться**</span><span class="sxs-lookup"><span data-stu-id="8162b-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="8162b-116">Тип: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="8162b-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="8162b-117">Непрозрачный маркер объекта индексатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="8162b-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8162b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8162b-118">Requirements</span></span>



| <span data-ttu-id="8162b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8162b-119">Requirement</span></span> | <span data-ttu-id="8162b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8162b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8162b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8162b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8162b-122">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="8162b-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8162b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8162b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8162b-124">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="8162b-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8162b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8162b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8162b-126"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="8162b-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8162b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8162b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8162b-128">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="8162b-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

