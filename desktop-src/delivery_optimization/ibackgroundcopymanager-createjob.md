---
title: Метод IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Создает задание.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Метод CreateJob
- Метод CreateJob, интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, метод CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/27/2021
ms.locfileid: "104081649"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="e4edf-106">Метод Ибаккграундкопиманажер:: CreateJob</span><span class="sxs-lookup"><span data-stu-id="e4edf-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="e4edf-107">Создает задание.</span><span class="sxs-lookup"><span data-stu-id="e4edf-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4edf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4edf-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="e4edf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4edf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4edf-110">*пдисплайнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4edf-111">Строка, завершающаяся нулем, которая содержит отображаемое имя для задания.</span><span class="sxs-lookup"><span data-stu-id="e4edf-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="e4edf-112">Как правило, отображаемое имя используется для распознавания задания в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e4edf-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="e4edf-113">Обратите внимание, что более одного задания могут иметь одно и то же отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="e4edf-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="e4edf-114">Не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4edf-114">Must not be **NULL**.</span></span> <span data-ttu-id="e4edf-115">Длина имени ограничена 256 символами, не включая знак завершения null.</span><span class="sxs-lookup"><span data-stu-id="e4edf-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="e4edf-116">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4edf-117">Тип задания перемещения, например BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="e4edf-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="e4edf-118">Список типов перемещения см. в разделе Перечисление [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="e4edf-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e4edf-119">*пжобид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4edf-120">Уникально идентифицирует задание в очереди.</span><span class="sxs-lookup"><span data-stu-id="e4edf-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="e4edf-121">Используйте этот идентификатор при вызове метода [**ибаккграундкопиманажер:: жетжоб**](ibackgroundcopymanager-getjob.md) для получения задания из очереди.</span><span class="sxs-lookup"><span data-stu-id="e4edf-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="e4edf-122">*ппжоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4edf-123">Указатель интерфейса [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md) , который используется для изменения свойств задания и указания файлов для передачи.</span><span class="sxs-lookup"><span data-stu-id="e4edf-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="e4edf-124">Чтобы активировать задание в очереди, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="e4edf-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="e4edf-125">Выпустите *ппжоб* по завершении.</span><span class="sxs-lookup"><span data-stu-id="e4edf-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4edf-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4edf-126">Return value</span></span>

<span data-ttu-id="e4edf-127">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="e4edf-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="e4edf-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e4edf-128">Return code</span></span>                                                                              | <span data-ttu-id="e4edf-129">Описание</span><span class="sxs-lookup"><span data-stu-id="e4edf-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e4edf-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e4edf-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="e4edf-131">Новое задание успешно создано.</span><span class="sxs-lookup"><span data-stu-id="e4edf-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4edf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4edf-132">Remarks</span></span>

<span data-ttu-id="e4edf-133">Только пользователь, создающий задание или пользователь с правами администратора, может [добавлять файлы в задание](https://www.bing.com/search?q=add+files+to+the+job) и [изменять свойства задания](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="e4edf-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4edf-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e4edf-134">Requirements</span></span>



| <span data-ttu-id="e4edf-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e4edf-135">Requirement</span></span> | <span data-ttu-id="e4edf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e4edf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4edf-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4edf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e4edf-138">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e4edf-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4edf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e4edf-140">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e4edf-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e4edf-141">Header</span><span class="sxs-lookup"><span data-stu-id="e4edf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4edf-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4edf-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4edf-143">IDL</span><span class="sxs-lookup"><span data-stu-id="e4edf-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4edf-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4edf-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4edf-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4edf-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4edf-146"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4edf-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e4edf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e4edf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4edf-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4edf-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e4edf-149">IID</span><span class="sxs-lookup"><span data-stu-id="e4edf-149">IID</span></span><br/>                      | <span data-ttu-id="e4edf-150">IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="e4edf-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e4edf-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4edf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4edf-152">**ибаккграундкопиманажер**</span><span class="sxs-lookup"><span data-stu-id="e4edf-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="e4edf-153">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="e4edf-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="e4edf-154">**Использованием метода ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="e4edf-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
