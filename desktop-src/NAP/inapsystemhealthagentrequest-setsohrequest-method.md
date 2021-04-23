---
title: Метод Инапсистемхеалсажентрекуест Сетсохрекуест (Напсистемхеалсажент. h)
description: Используется агентами работоспособности для записи своего запроса SoH, полученного в результате вызова Инапсистемхеалсаженткаллбакк Жетсохрекуест.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Метод Сетсохрекуест NAP
- Метод Сетсохрекуест NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Сетсохрекуест
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650370"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="cd35a-106">Метод Инапсистемхеалсажентрекуест:: Сетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="cd35a-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="cd35a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd35a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cd35a-108">Метод **инапсистемхеалсажентрекуест:: сетсохрекуест** используется агентами работоспособности для записи своего запроса SoH, полученного в результате вызова [**Инапсистемхеалсаженткаллбакк:: жетсохрекуест**](inapsystemhealthagentcallback-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="cd35a-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd35a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd35a-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="cd35a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd35a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd35a-111">*сохрекуест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd35a-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd35a-112">Указатель на пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="cd35a-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="cd35a-113">*качесохфорлатерусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd35a-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd35a-114">**Логическое** значение, равное **true** , если напажент должен кэшировать [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cd35a-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd35a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd35a-115">Return value</span></span>

<span data-ttu-id="cd35a-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="cd35a-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cd35a-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd35a-117">Return code</span></span>                                                                                     | <span data-ttu-id="cd35a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cd35a-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd35a-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cd35a-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="cd35a-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cd35a-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cd35a-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="cd35a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cd35a-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cd35a-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd35a-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd35a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cd35a-125">Requirements</span></span>



| <span data-ttu-id="cd35a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cd35a-126">Requirement</span></span> | <span data-ttu-id="cd35a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cd35a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd35a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd35a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd35a-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd35a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd35a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd35a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd35a-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd35a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd35a-132">Header</span><span class="sxs-lookup"><span data-stu-id="cd35a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd35a-133"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd35a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="cd35a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd35a-135"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="cd35a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd35a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd35a-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd35a-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="cd35a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd35a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd35a-139">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="cd35a-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





