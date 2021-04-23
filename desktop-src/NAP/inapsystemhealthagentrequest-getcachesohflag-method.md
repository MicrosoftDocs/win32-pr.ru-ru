---
title: Метод Инапсистемхеалсажентрекуест Жеткачесохфлаг (Напсистемхеалсажент. h)
description: Используется только Напажент.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Метод Жеткачесохфлаг NAP
- Метод Жеткачесохфлаг NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Жеткачесохфлаг
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534805"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="49916-106">Метод Инапсистемхеалсажентрекуест:: Жеткачесохфлаг</span><span class="sxs-lookup"><span data-stu-id="49916-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="49916-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="49916-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="49916-108">Метод **инапсистемхеалсажентрекуест:: жеткачесохфлаг** используется только напажент.</span><span class="sxs-lookup"><span data-stu-id="49916-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="49916-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49916-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="49916-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="49916-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49916-111">*качесохфорлатерусе*</span><span class="sxs-lookup"><span data-stu-id="49916-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="49916-112">**Логическое** значение, равное **true** , если напажент должен кэшировать [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="49916-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49916-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49916-113">Return value</span></span>

<span data-ttu-id="49916-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="49916-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="49916-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="49916-115">Return code</span></span>                                                                                     | <span data-ttu-id="49916-116">Описание</span><span class="sxs-lookup"><span data-stu-id="49916-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="49916-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="49916-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="49916-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="49916-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="49916-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="49916-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="49916-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="49916-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="49916-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="49916-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="49916-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49916-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="49916-123">Требования</span><span class="sxs-lookup"><span data-stu-id="49916-123">Requirements</span></span>



| <span data-ttu-id="49916-124">Требование</span><span class="sxs-lookup"><span data-stu-id="49916-124">Requirement</span></span> | <span data-ttu-id="49916-125">Значение</span><span class="sxs-lookup"><span data-stu-id="49916-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49916-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49916-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49916-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49916-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49916-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49916-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49916-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49916-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49916-130">Header</span><span class="sxs-lookup"><span data-stu-id="49916-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="49916-131"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="49916-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="49916-132">IDL</span><span class="sxs-lookup"><span data-stu-id="49916-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49916-133"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49916-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="49916-134">DLL</span><span class="sxs-lookup"><span data-stu-id="49916-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49916-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49916-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="49916-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49916-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49916-137">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="49916-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





