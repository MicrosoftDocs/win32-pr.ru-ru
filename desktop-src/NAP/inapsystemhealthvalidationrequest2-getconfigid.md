---
title: Метод INapSystemHealthValidationRequest2 Жетконфигид (Напсистемхеалсвалидатор. h)
description: Используется средствами проверки работоспособности системы (SHV) для получения идентификатора конфигурации в запросе на проверку.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Метод Жетконфигид NAP
- Метод Жетконфигид NAP, интерфейс INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 интерфейса NAP, метод Жетконфигид
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672867"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="82d1e-106">Метод INapSystemHealthValidationRequest2:: Жетконфигид</span><span class="sxs-lookup"><span data-stu-id="82d1e-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="82d1e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="82d1e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82d1e-108">Метод **INapSystemHealthValidationRequest2:: жетконфигид** используется средствами проверки работоспособности системы (SHV) для получения идентификатора конфигурации в запросе на проверку.</span><span class="sxs-lookup"><span data-stu-id="82d1e-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d1e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82d1e-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="82d1e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="82d1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d1e-111">*конфигид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82d1e-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82d1e-112">При возвращении — указатель на UINT32, содержащий идентификатор конфигурации SHV.</span><span class="sxs-lookup"><span data-stu-id="82d1e-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d1e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82d1e-113">Return value</span></span>

<span data-ttu-id="82d1e-114">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="82d1e-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="82d1e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="82d1e-115">Return code</span></span>                                                                                  | <span data-ttu-id="82d1e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="82d1e-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="82d1e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="82d1e-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="82d1e-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="82d1e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="82d1e-120">Параметр Конфигид имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="82d1e-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="82d1e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="82d1e-121">Requirements</span></span>



| <span data-ttu-id="82d1e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="82d1e-122">Requirement</span></span> | <span data-ttu-id="82d1e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="82d1e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d1e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82d1e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82d1e-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="82d1e-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="82d1e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82d1e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82d1e-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="82d1e-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="82d1e-128">Header</span><span class="sxs-lookup"><span data-stu-id="82d1e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d1e-129"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="82d1e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="82d1e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82d1e-131"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="82d1e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="82d1e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d1e-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="82d1e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82d1e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d1e-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="82d1e-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





