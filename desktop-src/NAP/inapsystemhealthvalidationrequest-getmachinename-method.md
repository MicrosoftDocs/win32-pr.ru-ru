---
title: Метод Инапсистемхеалсвалидатионрекуест Жетмачиненаме (Напсистемхеалсвалидатор. h)
description: Используется средствами проверки работоспособности системы (SHV) для получения имени компьютера клиента NAP. Затем SHV записывает эти сведения в журнал.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Метод Жетмачиненаме NAP
- Метод Жетмачиненаме NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетмачиненаме
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137783"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="3433c-107">Метод Инапсистемхеалсвалидатионрекуест:: Жетмачиненаме</span><span class="sxs-lookup"><span data-stu-id="3433c-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="3433c-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="3433c-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3433c-109">Метод **инапсистемхеалсвалидатионрекуест:: жетмачиненаме** используется средствами проверки работоспособности системы (SHV) для получения имени компьютера клиента NAP.</span><span class="sxs-lookup"><span data-stu-id="3433c-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="3433c-110">Затем SHV записывает эти сведения в журнал.</span><span class="sxs-lookup"><span data-stu-id="3433c-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3433c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3433c-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="3433c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3433c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3433c-113">*MachineName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3433c-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3433c-114">Указатель на указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащую имя компьютера клиента NAP.</span><span class="sxs-lookup"><span data-stu-id="3433c-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3433c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3433c-115">Return value</span></span>

<span data-ttu-id="3433c-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="3433c-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3433c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3433c-117">Return code</span></span>                                                                                     | <span data-ttu-id="3433c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3433c-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3433c-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3433c-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="3433c-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3433c-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3433c-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="3433c-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3433c-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3433c-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3433c-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3433c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3433c-125">Requirements</span></span>



| <span data-ttu-id="3433c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3433c-126">Requirement</span></span> | <span data-ttu-id="3433c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3433c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3433c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3433c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3433c-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3433c-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="3433c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3433c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3433c-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3433c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3433c-132">Header</span><span class="sxs-lookup"><span data-stu-id="3433c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3433c-133"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="3433c-134">IDL</span><span class="sxs-lookup"><span data-stu-id="3433c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3433c-135"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="3433c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3433c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3433c-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3433c-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="3433c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3433c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3433c-139">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="3433c-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





