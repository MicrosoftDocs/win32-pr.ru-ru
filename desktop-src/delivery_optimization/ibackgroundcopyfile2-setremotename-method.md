---
title: Метод IBackgroundCopyFile2 Сетремотенаме (Deliveryoptimization. h)
description: Изменяет удаленное имя на новый URL-адрес в задании загрузки.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Метод Сетремотенаме
- Метод Сетремотенаме, интерфейс IBackgroundCopyFile2
- Интерфейс IBackgroundCopyFile2, метод Сетремотенаме
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490257"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="716f7-106">Метод IBackgroundCopyFile2:: Сетремотенаме</span><span class="sxs-lookup"><span data-stu-id="716f7-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="716f7-107">Изменяет удаленное имя на новый URL-адрес в задании загрузки.</span><span class="sxs-lookup"><span data-stu-id="716f7-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="716f7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="716f7-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="716f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="716f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716f7-110">*Ремотенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="716f7-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716f7-111">Строка, заканчивающаяся нулем и содержащая имя файла на сервере.</span><span class="sxs-lookup"><span data-stu-id="716f7-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="716f7-112">Сведения об указании удаленного имени см. в разделе элемент **ремотенаме** .</span><span class="sxs-lookup"><span data-stu-id="716f7-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716f7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="716f7-113">Return value</span></span>

<span data-ttu-id="716f7-114">Этот метод возвращает следующие возвращаемые значения, а также другие.</span><span class="sxs-lookup"><span data-stu-id="716f7-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="716f7-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="716f7-115">Return code</span></span>                                                                                  | <span data-ttu-id="716f7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="716f7-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="716f7-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="716f7-118">Успешно</span><span class="sxs-lookup"><span data-stu-id="716f7-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="716f7-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="716f7-120">Новое удаленное имя является недопустимым URL-адресом, или новый URL-адрес слишком длинный (длина URL-адреса не должна превышать 2 200 символов).</span><span class="sxs-lookup"><span data-stu-id="716f7-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="716f7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="716f7-121">Remarks</span></span>

<span data-ttu-id="716f7-122">Как правило, этот метод вызывается, если требуется изменить URL-адрес, используемый для перемещения файла, или если необходимо изменить имя или путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="716f7-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="716f7-123">Этот метод не выполняет сериализацию при возврате.</span><span class="sxs-lookup"><span data-stu-id="716f7-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="716f7-124">Чтобы сериализовать изменение, [**приостановите**](ibackgroundcopyjob-suspend.md) задание, вызовите этот метод (если изменяется несколько файлов в задании, используйте цикл) и [**возобновите**](ibackgroundcopyjob-resume.md) задание.</span><span class="sxs-lookup"><span data-stu-id="716f7-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="716f7-125">Вызов метода **использованием метода ibackgroundcopyjob:: Resume** сериализует изменение.</span><span class="sxs-lookup"><span data-stu-id="716f7-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="716f7-126">Если метка времени или размер файла нового удаленного имени отличаются от предыдущего удаленного имени, либо новый сервер не поддерживает возобновление контрольной точки (для удаленных имен HTTP), выполните загрузку повторно.</span><span class="sxs-lookup"><span data-stu-id="716f7-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="716f7-127">В противном случае перемещение возобновляется с той же самой позицией на новом сервере.</span><span class="sxs-lookup"><span data-stu-id="716f7-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="716f7-128">Не перезапускают уже передаваемые файлы.</span><span class="sxs-lookup"><span data-stu-id="716f7-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="716f7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="716f7-129">Requirements</span></span>



| <span data-ttu-id="716f7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="716f7-130">Requirement</span></span> | <span data-ttu-id="716f7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="716f7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="716f7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="716f7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="716f7-133">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="716f7-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="716f7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="716f7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="716f7-135">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="716f7-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="716f7-136">Header</span><span class="sxs-lookup"><span data-stu-id="716f7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="716f7-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="716f7-138">IDL</span><span class="sxs-lookup"><span data-stu-id="716f7-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="716f7-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="716f7-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="716f7-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="716f7-141"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="716f7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="716f7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="716f7-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="716f7-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="716f7-144">IID</span><span class="sxs-lookup"><span data-stu-id="716f7-144">IID</span></span><br/>                      | <span data-ttu-id="716f7-145">IID_IBackgroundCopyFile2 определен как 83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="716f7-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="716f7-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="716f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716f7-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="716f7-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





