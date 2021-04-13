---
title: Метод INapEnforcementClientConnection2 Жетинсталледшвс (Напенфорцементклиент. h)
description: Используется агентом NAP для запроса установленных средств проверки работоспособности системы (SHV) на клиенте.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Метод Жетинсталледшвс NAP
- Метод Жетинсталледшвс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Жетинсталледшвс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493248"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="579fb-106">Метод INapEnforcementClientConnection2:: Жетинсталледшвс</span><span class="sxs-lookup"><span data-stu-id="579fb-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="579fb-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="579fb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="579fb-108">Метод **жетинсталледшвс** используется агентом NAP для запроса установленных средств проверки работоспособности системы (SHV) на клиенте.</span><span class="sxs-lookup"><span data-stu-id="579fb-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="579fb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="579fb-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="579fb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="579fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579fb-111">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="579fb-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579fb-112">Указатель на значение [системхеалсентитикаунт](nap-datatypes.md) , указывающее число установленных SHV в *идентификаторах*.</span><span class="sxs-lookup"><span data-stu-id="579fb-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="579fb-113">*идентификаторы* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="579fb-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579fb-114">Указатель на массив значений [системхеалсентитид](nap-datatypes.md) , содержащих установленные идентификаторы SHV.</span><span class="sxs-lookup"><span data-stu-id="579fb-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579fb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="579fb-115">Return value</span></span>

<span data-ttu-id="579fb-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="579fb-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="579fb-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="579fb-117">Return code</span></span>                                                                                   | <span data-ttu-id="579fb-118">Описание</span><span class="sxs-lookup"><span data-stu-id="579fb-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="579fb-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="579fb-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="579fb-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="579fb-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="579fb-121"><dt>**Д \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="579fb-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="579fb-122">Методу передан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="579fb-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="579fb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="579fb-123">Requirements</span></span>



| <span data-ttu-id="579fb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="579fb-124">Requirement</span></span> | <span data-ttu-id="579fb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="579fb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579fb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="579fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="579fb-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="579fb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="579fb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="579fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="579fb-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="579fb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="579fb-130">Header</span><span class="sxs-lookup"><span data-stu-id="579fb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="579fb-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="579fb-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="579fb-132">IDL</span><span class="sxs-lookup"><span data-stu-id="579fb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="579fb-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="579fb-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="579fb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="579fb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579fb-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579fb-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="579fb-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="579fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579fb-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="579fb-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





