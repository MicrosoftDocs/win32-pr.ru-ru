---
title: ResourceLocator. Клеароптионс, метод (Всмандисп. h)
description: Удаляет все параметры из объекта ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Клеароптионс
- Служба удаленного управления Windows метода Клеароптионс, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Клеароптионс
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891569"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="5a91f-106">ResourceLocator. Клеароптионс, метод</span><span class="sxs-lookup"><span data-stu-id="5a91f-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="5a91f-107">Удаляет все [*Параметры*](windows-remote-management-glossary.md) из объекта [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5a91f-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="5a91f-108">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="5a91f-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a91f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a91f-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="5a91f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a91f-110">Parameters</span></span>

<span data-ttu-id="5a91f-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5a91f-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a91f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a91f-112">Remarks</span></span>

<span data-ttu-id="5a91f-113">**Ивсманресаурцелокатор:: клеароптионс** — соответствующий метод C++.</span><span class="sxs-lookup"><span data-stu-id="5a91f-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a91f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5a91f-114">Requirements</span></span>



| <span data-ttu-id="5a91f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5a91f-115">Requirement</span></span> | <span data-ttu-id="5a91f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5a91f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a91f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a91f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a91f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a91f-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5a91f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a91f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a91f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a91f-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5a91f-121">Header</span><span class="sxs-lookup"><span data-stu-id="5a91f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a91f-122"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a91f-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a91f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5a91f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a91f-124"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a91f-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5a91f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a91f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a91f-126"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a91f-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a91f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5a91f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a91f-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a91f-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a91f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a91f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a91f-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="5a91f-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





