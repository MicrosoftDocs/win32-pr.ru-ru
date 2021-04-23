---
title: Интерфейс Ибаккграундкопифиле (Deliveryoptimization. h)
description: Ибаккграундкопифиле содержит сведения о файле, который является частью задания. Например, можно использовать методы Ибаккграундкопифиле для получения локальных и удаленных имен файла и сведений о ходе выполнения.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701039"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="eb904-106">Интерфейс Ибаккграундкопифиле</span><span class="sxs-lookup"><span data-stu-id="eb904-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="eb904-107">**Ибаккграундкопифиле** содержит сведения о файле, который является частью задания.</span><span class="sxs-lookup"><span data-stu-id="eb904-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="eb904-108">Например, можно использовать методы **ибаккграундкопифиле** для получения локальных и удаленных имен файла и сведений о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb904-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="eb904-109">Чтобы получить указатель интерфейса **ибаккграундкопифиле** , вызовите метод [**Ибаккграундкоперрор::**](ibackgroundcopyerror-getfile-method.md) GetNext или метод [**иенумбаккграундкопифилес:: Next**](ienumbackgroundcopyfiles-next.md) .</span><span class="sxs-lookup"><span data-stu-id="eb904-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="eb904-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="eb904-110">Members</span></span>

<span data-ttu-id="eb904-111">Интерфейс **ибаккграундкопифиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eb904-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eb904-112">**Ибаккграундкопифиле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eb904-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="eb904-113">Методы</span><span class="sxs-lookup"><span data-stu-id="eb904-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb904-114">Методы</span><span class="sxs-lookup"><span data-stu-id="eb904-114">Methods</span></span>

<span data-ttu-id="eb904-115">Интерфейс **ибаккграундкопифиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="eb904-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="eb904-116">Метод</span><span class="sxs-lookup"><span data-stu-id="eb904-116">Method</span></span>                                                            | <span data-ttu-id="eb904-117">Описание</span><span class="sxs-lookup"><span data-stu-id="eb904-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="eb904-118">**жетлокалнаме**</span><span class="sxs-lookup"><span data-stu-id="eb904-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="eb904-119">Возвращает локальное имя файла.</span><span class="sxs-lookup"><span data-stu-id="eb904-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="eb904-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="eb904-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="eb904-121">Возвращает ход выполнения перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="eb904-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="eb904-122">**жетремотенаме**</span><span class="sxs-lookup"><span data-stu-id="eb904-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="eb904-123">Извлекает удаленное имя файла.</span><span class="sxs-lookup"><span data-stu-id="eb904-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="eb904-124">Требования</span><span class="sxs-lookup"><span data-stu-id="eb904-124">Requirements</span></span>



| <span data-ttu-id="eb904-125">Требование</span><span class="sxs-lookup"><span data-stu-id="eb904-125">Requirement</span></span> | <span data-ttu-id="eb904-126">Значение</span><span class="sxs-lookup"><span data-stu-id="eb904-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb904-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb904-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb904-128">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="eb904-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eb904-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb904-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb904-130">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="eb904-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eb904-131">Header</span><span class="sxs-lookup"><span data-stu-id="eb904-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb904-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb904-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb904-133">IDL</span><span class="sxs-lookup"><span data-stu-id="eb904-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb904-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb904-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="eb904-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb904-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb904-136"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb904-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="eb904-137">DLL</span><span class="sxs-lookup"><span data-stu-id="eb904-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb904-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb904-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="eb904-139">IID</span><span class="sxs-lookup"><span data-stu-id="eb904-139">IID</span></span><br/>                      | <span data-ttu-id="eb904-140">IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="eb904-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="eb904-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb904-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb904-142">**ибаккграундкоперрор**</span><span class="sxs-lookup"><span data-stu-id="eb904-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="eb904-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="eb904-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="eb904-144">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="eb904-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="eb904-145">**иенумбаккграундкопифилес**</span><span class="sxs-lookup"><span data-stu-id="eb904-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

