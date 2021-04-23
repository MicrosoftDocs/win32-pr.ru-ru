---
title: Свойство ResourceLocator. Мустундерстандоптионс (Всмандисп. h)
description: Возвращает или задает значение Мустундерстандоптионс для объекта ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Мустундерстандоптионс
- Служба удаленного управления Windows свойства Мустундерстандоптионс, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство Мустундерстандоптионс
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989238"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="4fff6-106">ResourceLocator. Мустундерстандоптионс, свойство</span><span class="sxs-lookup"><span data-stu-id="4fff6-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="4fff6-107">Возвращает или задает значение **мустундерстандоптионс** для объекта [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="4fff6-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="4fff6-108">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="4fff6-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="4fff6-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4fff6-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fff6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fff6-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="4fff6-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fff6-111">Property value</span></span>

<span data-ttu-id="4fff6-112">Указывает, что при **значении true** служба, которая реализует [протокол WS-Management](ws-management-protocol.md) , должна возвращать ошибку, если она не может обработать параметр.</span><span class="sxs-lookup"><span data-stu-id="4fff6-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fff6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fff6-113">Remarks</span></span>

<span data-ttu-id="4fff6-114">**Ивсманресаурцелокатор:: мустундерстандоптионс** — соответствующее свойство C++.</span><span class="sxs-lookup"><span data-stu-id="4fff6-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fff6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4fff6-115">Requirements</span></span>



| <span data-ttu-id="4fff6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4fff6-116">Requirement</span></span> | <span data-ttu-id="4fff6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4fff6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fff6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fff6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4fff6-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fff6-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4fff6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fff6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4fff6-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fff6-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4fff6-122">Header</span><span class="sxs-lookup"><span data-stu-id="4fff6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fff6-123"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fff6-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fff6-124">IDL</span><span class="sxs-lookup"><span data-stu-id="4fff6-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fff6-125"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fff6-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4fff6-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fff6-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fff6-127"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fff6-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fff6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4fff6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fff6-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fff6-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fff6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fff6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fff6-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="4fff6-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





