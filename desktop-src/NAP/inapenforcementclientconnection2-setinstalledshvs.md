---
title: Метод INapEnforcementClientConnection2 Сетинсталледшвс (Напенфорцементклиент. h)
description: Используется агентом NAP для установки на клиенте установленных средств проверки работоспособности системы (SHV).
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Метод Сетинсталледшвс NAP
- Метод Сетинсталледшвс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Сетинсталледшвс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137787"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="9d317-106">Метод INapEnforcementClientConnection2:: Сетинсталледшвс</span><span class="sxs-lookup"><span data-stu-id="9d317-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="9d317-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d317-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9d317-108">Метод **сетинсталледшвс** используется агентом NAP для установки на клиенте установленных средств проверки работоспособности системы (SHV).</span><span class="sxs-lookup"><span data-stu-id="9d317-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d317-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d317-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="9d317-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d317-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d317-111">*количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d317-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d317-112">Значение [системхеалсентитикаунт](nap-datatypes.md) , указывающее количество средств SHV для установки в *идентификаторах*.</span><span class="sxs-lookup"><span data-stu-id="9d317-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="9d317-113">*идентификаторы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d317-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d317-114">Указатель на значение [системхеалсентитид](nap-datatypes.md) , содержащее список идентификаторов SHV для установки.</span><span class="sxs-lookup"><span data-stu-id="9d317-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d317-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d317-115">Return value</span></span>

<span data-ttu-id="9d317-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="9d317-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9d317-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9d317-117">Return code</span></span>                                                                                  | <span data-ttu-id="9d317-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9d317-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9d317-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9d317-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="9d317-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9d317-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="9d317-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d317-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9d317-122">Параметр *Count* равен 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="9d317-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d317-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9d317-123">Requirements</span></span>



| <span data-ttu-id="9d317-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9d317-124">Requirement</span></span> | <span data-ttu-id="9d317-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9d317-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d317-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d317-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d317-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d317-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d317-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d317-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d317-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d317-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d317-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d317-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d317-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d317-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d317-132">IDL</span><span class="sxs-lookup"><span data-stu-id="9d317-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d317-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d317-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d317-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d317-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d317-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d317-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9d317-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d317-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d317-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="9d317-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





