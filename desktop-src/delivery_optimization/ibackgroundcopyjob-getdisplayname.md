---
title: Метод использованием метода ibackgroundcopyjob DisplayName (Deliveryoptimization. h)
description: Извлекает отображаемое имя для задания. Обычно отображаемое имя используется для распознавания задания в пользовательском интерфейсе.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName - метод
- Метод использованием метода ibackgroundcopyjob, интерфейс
- Интерфейс использованием метода ibackgroundcopyjob, метод "DisplayName"
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989135"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="e2df5-107">Метод использованием метода ibackgroundcopyjob:: DisplayName</span><span class="sxs-lookup"><span data-stu-id="e2df5-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="e2df5-108">Извлекает отображаемое имя для задания.</span><span class="sxs-lookup"><span data-stu-id="e2df5-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="e2df5-109">Обычно отображаемое имя используется для распознавания задания в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e2df5-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2df5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2df5-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="e2df5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2df5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2df5-112">*ппдисплайнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2df5-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2df5-113">Строка, завершающаяся нулем, которая содержит отображаемое имя, идентифицирующее задание.</span><span class="sxs-lookup"><span data-stu-id="e2df5-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="e2df5-114">Более одного задания могут иметь одно и то же отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="e2df5-114">More than one job can have the same display name.</span></span> <span data-ttu-id="e2df5-115">Вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить *ппдисплайнаме* по завершении.</span><span class="sxs-lookup"><span data-stu-id="e2df5-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2df5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2df5-116">Return value</span></span>

<span data-ttu-id="e2df5-117">Этот метод возвращает следующие значения **HRESULT** , а также другие.</span><span class="sxs-lookup"><span data-stu-id="e2df5-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="e2df5-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e2df5-118">Return code</span></span>                                                                                  | <span data-ttu-id="e2df5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e2df5-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="e2df5-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="e2df5-121">Отображаемое имя успешно получено.</span><span class="sxs-lookup"><span data-stu-id="e2df5-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="e2df5-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e2df5-123">Параметр *ппдисплайнаме* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2df5-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2df5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e2df5-124">Requirements</span></span>



| <span data-ttu-id="e2df5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e2df5-125">Requirement</span></span> | <span data-ttu-id="e2df5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e2df5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2df5-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2df5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2df5-128">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e2df5-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2df5-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2df5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2df5-130">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="e2df5-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e2df5-131">Header</span><span class="sxs-lookup"><span data-stu-id="e2df5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2df5-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2df5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="e2df5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2df5-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e2df5-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2df5-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2df5-136"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e2df5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e2df5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2df5-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2df5-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e2df5-139">IID</span><span class="sxs-lookup"><span data-stu-id="e2df5-139">IID</span></span><br/>                      | <span data-ttu-id="e2df5-140">IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="e2df5-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e2df5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2df5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2df5-142">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="e2df5-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

