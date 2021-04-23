---
title: Интерфейс Ибаккграундкоперрор (Deliveryoptimization. h)
description: Используйте интерфейс Ибаккграундкоперрор, чтобы определить причину ошибки, и если процесс перемещения может быть продолжен.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Интерфейс Ибаккграундкоперрор
- Интерфейс Ибаккграундкоперрор, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490263"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="d7783-105">Интерфейс Ибаккграундкоперрор</span><span class="sxs-lookup"><span data-stu-id="d7783-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="d7783-106">Используйте интерфейс **ибаккграундкоперрор** , чтобы определить причину ошибки, и если процесс перемещения может быть продолжен.</span><span class="sxs-lookup"><span data-stu-id="d7783-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="d7783-107">Создает объект Error только в том случае, если состояние задания — BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="d7783-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="d7783-108">Не создает объект Error при сбое метода интерфейса **ибаккграундкопикскскскс** .</span><span class="sxs-lookup"><span data-stu-id="d7783-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="d7783-109">Объект Error доступен до тех пор, пока не начнется передача данных (состояние задания меняется на BG_JOB_STATE_TRANSFERRING) для задания.</span><span class="sxs-lookup"><span data-stu-id="d7783-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="d7783-110">Чтобы получить объект **ибаккграундкоперрор** , вызовите метод [**использованием метода ibackgroundcopyjob::**](ibackgroundcopyjob-geterror.md) GetObject.</span><span class="sxs-lookup"><span data-stu-id="d7783-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="d7783-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="d7783-111">Members</span></span>

<span data-ttu-id="d7783-112">Интерфейс **ибаккграундкоперрор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d7783-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d7783-113">**Ибаккграундкоперрор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d7783-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="d7783-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d7783-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7783-115">Методы</span><span class="sxs-lookup"><span data-stu-id="d7783-115">Methods</span></span>

<span data-ttu-id="d7783-116">Интерфейс **ибаккграундкоперрор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d7783-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="d7783-117">Метод</span><span class="sxs-lookup"><span data-stu-id="d7783-117">Method</span></span>                                                   | <span data-ttu-id="d7783-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d7783-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7783-119">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="d7783-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="d7783-120">Извлекает код ошибки и определяет контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d7783-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="d7783-121">**Файл.**</span><span class="sxs-lookup"><span data-stu-id="d7783-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="d7783-122">Извлекает указатель интерфейса на объект File, связанный с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d7783-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="d7783-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d7783-123">Requirements</span></span>



| <span data-ttu-id="d7783-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d7783-124">Requirement</span></span> | <span data-ttu-id="d7783-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d7783-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7783-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7783-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7783-127">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d7783-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7783-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7783-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7783-129">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d7783-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7783-130">Header</span><span class="sxs-lookup"><span data-stu-id="d7783-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7783-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7783-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7783-132">IDL</span><span class="sxs-lookup"><span data-stu-id="d7783-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7783-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7783-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7783-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7783-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7783-135"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7783-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d7783-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d7783-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7783-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7783-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d7783-138">IID</span><span class="sxs-lookup"><span data-stu-id="d7783-138">IID</span></span><br/>                      | <span data-ttu-id="d7783-139">IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="d7783-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d7783-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7783-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7783-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="d7783-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="d7783-142">**Использованием метода ibackgroundcopyjob:: возникла ошибка**</span><span class="sxs-lookup"><span data-stu-id="d7783-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="d7783-143">**Использованием метода ibackgroundcopyjob:: State**</span><span class="sxs-lookup"><span data-stu-id="d7783-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="d7783-144">**Ибаккграундкопикаллбакк:: Жоберрор**</span><span class="sxs-lookup"><span data-stu-id="d7783-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

