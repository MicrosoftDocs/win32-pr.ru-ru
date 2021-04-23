---
title: Бесплатный метод Имеморяллокатор
description: Метод Free освобождает память, выделенную методом выделения.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Структурированное хранилище методов Free
- Структурированное хранилище методов Free, интерфейс Имеморяллокатор
- Имеморяллокатор интерфейс структурированного хранилища, Бесплатный метод
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071222"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="d93eb-106">Метод Имеморяллокатор:: Free</span><span class="sxs-lookup"><span data-stu-id="d93eb-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="d93eb-107">Метод **Free** освобождает память, выделенную методом [**выделения**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="d93eb-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93eb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d93eb-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="d93eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d93eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93eb-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="d93eb-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="d93eb-111">Указатель на память, которую необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="d93eb-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d93eb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d93eb-112">Requirements</span></span>



| <span data-ttu-id="d93eb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d93eb-113">Requirement</span></span> | <span data-ttu-id="d93eb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d93eb-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d93eb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d93eb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d93eb-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d93eb-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d93eb-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d93eb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d93eb-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d93eb-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d93eb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d93eb-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="d93eb-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d93eb-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





