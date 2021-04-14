---
description: Определяет метод, который определяет, будет ли оболочка разрешать перемещение, копирование, удаление или переименование папки в корне синхронизации поставщика облачных служб.
title: Интерфейс IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415277"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="405b9-103">Интерфейс IStorageProviderCopyHook</span><span class="sxs-lookup"><span data-stu-id="405b9-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="405b9-104">Предоставляет метод, определяющий, будет ли оболочка разрешать перемещение, копирование, удаление или переименование папки в корне синхронизации поставщика облачных служб.</span><span class="sxs-lookup"><span data-stu-id="405b9-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="405b9-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="405b9-105">Members</span></span>

<span data-ttu-id="405b9-106">Интерфейс **исторажепровидеркопихук** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="405b9-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="405b9-107">**Исторажепровидеркопихук** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="405b9-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="405b9-108">Методы</span><span class="sxs-lookup"><span data-stu-id="405b9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="405b9-109">Методы</span><span class="sxs-lookup"><span data-stu-id="405b9-109">Methods</span></span>

<span data-ttu-id="405b9-110">Интерфейс **исторажепровидеркопихук** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="405b9-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="405b9-111">Метод</span><span class="sxs-lookup"><span data-stu-id="405b9-111">Method</span></span>                                           | <span data-ttu-id="405b9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="405b9-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="405b9-113">**копикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="405b9-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="405b9-114">Определяет, будет ли оболочка разрешать перемещение, копирование, удаление или переименование папки в корне синхронизации поставщика облачных служб.</span><span class="sxs-lookup"><span data-stu-id="405b9-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="405b9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="405b9-115">Requirements</span></span>

| <span data-ttu-id="405b9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="405b9-116">Requirement</span></span> | <span data-ttu-id="405b9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="405b9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="405b9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="405b9-118">Minimum supported client</span></span> | <span data-ttu-id="405b9-119">Windows 10 Insider Preview Build 19624</span><span class="sxs-lookup"><span data-stu-id="405b9-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="405b9-120">Header</span><span class="sxs-lookup"><span data-stu-id="405b9-120">Header</span></span><br/>                   | <span data-ttu-id="405b9-121">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="405b9-121">shobjidl.h</span></span>   |
