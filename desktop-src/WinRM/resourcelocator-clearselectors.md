---
title: ResourceLocator. Клеарселекторс, метод (Всмандисп. h)
description: Удаляет все селекторы из объекта ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Клеарселекторс
- Служба удаленного управления Windows метода Клеарселекторс, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Клеарселекторс
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137198"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="4f331-106">ResourceLocator. Клеарселекторс, метод</span><span class="sxs-lookup"><span data-stu-id="4f331-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="4f331-107">Удаляет все [*селекторы*](windows-remote-management-glossary.md) из объекта [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="4f331-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="4f331-108">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="4f331-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f331-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f331-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="4f331-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f331-110">Parameters</span></span>

<span data-ttu-id="4f331-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4f331-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f331-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f331-112">Remarks</span></span>

<span data-ttu-id="4f331-113">**Ивсманресаурцелокатор:: клеарселекторс** — соответствующий метод C++.</span><span class="sxs-lookup"><span data-stu-id="4f331-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f331-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4f331-114">Requirements</span></span>



| <span data-ttu-id="4f331-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4f331-115">Requirement</span></span> | <span data-ttu-id="4f331-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4f331-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f331-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f331-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4f331-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f331-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4f331-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f331-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4f331-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f331-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4f331-121">Header</span><span class="sxs-lookup"><span data-stu-id="4f331-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f331-122"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f331-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f331-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4f331-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f331-124"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f331-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f331-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f331-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f331-126"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f331-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f331-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4f331-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f331-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f331-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f331-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f331-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f331-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="4f331-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





