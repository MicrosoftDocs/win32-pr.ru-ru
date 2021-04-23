---
title: Интерфейс IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Используйте этот интерфейс для получения или задания общих свойств передачи файлов (DO) оптимизации доставки.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Интерфейс IBackgroundCopyFile5
- Интерфейс IBackgroundCopyFile5, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135739"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="5699c-105">Интерфейс IBackgroundCopyFile5</span><span class="sxs-lookup"><span data-stu-id="5699c-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="5699c-106">Используйте этот интерфейс для получения или задания общих свойств передачи файлов (DO) оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="5699c-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="5699c-107">Чтобы получить указатель интерфейса **IBackgroundCopyFile5** , вызовите метод **Ибаккграундкопифиле:: QueryInterface** , используя __uuidof (IBackgroundCopyFile5) для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5699c-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="5699c-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5699c-108">Members</span></span>

<span data-ttu-id="5699c-109">Интерфейс **IBackgroundCopyFile5** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5699c-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5699c-110">**IBackgroundCopyFile5** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5699c-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="5699c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5699c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5699c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5699c-112">Methods</span></span>

<span data-ttu-id="5699c-113">Интерфейс **IBackgroundCopyFile5** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5699c-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="5699c-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5699c-114">Method</span></span>                                                  | <span data-ttu-id="5699c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5699c-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="5699c-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="5699c-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="5699c-117">Возвращает значение универсального свойства Баккграундкопифиле.</span><span class="sxs-lookup"><span data-stu-id="5699c-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="5699c-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="5699c-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="5699c-119">Задает значение универсального свойства Баккграундкопифиле.</span><span class="sxs-lookup"><span data-stu-id="5699c-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5699c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5699c-120">Requirements</span></span>



| <span data-ttu-id="5699c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5699c-121">Requirement</span></span> | <span data-ttu-id="5699c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5699c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5699c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5699c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5699c-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="5699c-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5699c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5699c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5699c-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="5699c-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5699c-127">Header</span><span class="sxs-lookup"><span data-stu-id="5699c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5699c-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5699c-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5699c-129">IDL</span><span class="sxs-lookup"><span data-stu-id="5699c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5699c-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5699c-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5699c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5699c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5699c-132"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5699c-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5699c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5699c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5699c-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5699c-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5699c-135">IID</span><span class="sxs-lookup"><span data-stu-id="5699c-135">IID</span></span><br/>                      | <span data-ttu-id="5699c-136">IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="5699c-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5699c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5699c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5699c-138">**ибаккграундкопифиле**</span><span class="sxs-lookup"><span data-stu-id="5699c-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="5699c-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="5699c-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

