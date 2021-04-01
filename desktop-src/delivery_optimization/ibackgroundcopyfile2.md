---
title: Интерфейс IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Используйте интерфейс IBackgroundCopyFile2, чтобы указать новое удаленное имя для файла и получить список загружаемых диапазонов.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Интерфейс IBackgroundCopyFile2
- Интерфейс IBackgroundCopyFile2, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071536"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="8921f-105">Интерфейс IBackgroundCopyFile2</span><span class="sxs-lookup"><span data-stu-id="8921f-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="8921f-106">Используйте интерфейс **IBackgroundCopyFile2** , чтобы указать новое удаленное имя для файла и получить список загружаемых диапазонов.</span><span class="sxs-lookup"><span data-stu-id="8921f-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="8921f-107">Интерфейс **IBackgroundCopyFile2** наследуется от интерфейса [**ибаккграундкопифиле**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8921f-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="8921f-108">Чтобы получить указатель интерфейса **IBackgroundCopyFile2** , вызовите метод **Ибаккграундкопифиле:: QueryInterface** , используя __uuidof (IBackgroundCopyFile2) для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8921f-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="8921f-109">Используйте указатель интерфейса **IBackgroundCopyFile2** для вызова методов [**ибаккграундкопифиле**](ibackgroundcopyfile.md) и **IBackgroundCopyFile2** .</span><span class="sxs-lookup"><span data-stu-id="8921f-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="8921f-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="8921f-110">Members</span></span>

<span data-ttu-id="8921f-111">Интерфейс **IBackgroundCopyFile2** наследует от [**ибаккграундкопифиле**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="8921f-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="8921f-112">**IBackgroundCopyFile2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8921f-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="8921f-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8921f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8921f-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8921f-114">Methods</span></span>

<span data-ttu-id="8921f-115">Интерфейс **IBackgroundCopyFile2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8921f-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="8921f-116">Метод</span><span class="sxs-lookup"><span data-stu-id="8921f-116">Method</span></span>                                                             | <span data-ttu-id="8921f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8921f-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="8921f-118">**жетфилеранжес**</span><span class="sxs-lookup"><span data-stu-id="8921f-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="8921f-119">Извлекает массив диапазонов, которые необходимо загрузить из URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8921f-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="8921f-120">**сетремотенаме**</span><span class="sxs-lookup"><span data-stu-id="8921f-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="8921f-121">Изменяет удаленное имя на новый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="8921f-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="8921f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8921f-122">Requirements</span></span>



| <span data-ttu-id="8921f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8921f-123">Requirement</span></span> | <span data-ttu-id="8921f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8921f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8921f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8921f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8921f-126">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="8921f-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8921f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8921f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8921f-128">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="8921f-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8921f-129">Header</span><span class="sxs-lookup"><span data-stu-id="8921f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8921f-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8921f-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8921f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="8921f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8921f-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8921f-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8921f-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8921f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8921f-134"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8921f-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8921f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8921f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8921f-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8921f-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8921f-137">IID</span><span class="sxs-lookup"><span data-stu-id="8921f-137">IID</span></span><br/>                      | <span data-ttu-id="8921f-138">IID_IBackgroundCopyFile2 определен как 83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="8921f-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8921f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8921f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8921f-140">**ибаккграундкопифиле**</span><span class="sxs-lookup"><span data-stu-id="8921f-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





