---
title: Метод Инапсистемхеалсажентрекуест Жетсохрекуест (Напсистемхеалсажент. h)
description: Может использоваться SHA Get SoH, ранее кэшированный Напажент.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Метод Жетсохрекуест NAP
- Метод Жетсохрекуест NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Жетсохрекуест
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071950"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="49316-106">Метод Инапсистемхеалсажентрекуест:: Жетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="49316-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="49316-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="49316-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="49316-108">Метод **инапсистемхеалсажентрекуест:: жетсохрекуест** может использоваться SHA Get SoH, ранее кэшированный напажент.</span><span class="sxs-lookup"><span data-stu-id="49316-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="49316-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49316-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="49316-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="49316-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49316-111">*сохрекуест* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="49316-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49316-112">Указатель на указатель на [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="49316-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49316-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49316-113">Return value</span></span>

<span data-ttu-id="49316-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="49316-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="49316-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="49316-115">Return code</span></span>                                                                                            | <span data-ttu-id="49316-116">Описание</span><span class="sxs-lookup"><span data-stu-id="49316-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49316-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="49316-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="49316-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="49316-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="49316-119"><dt>**Защита доступа к сети \_ E \_ без \_ кэшированного \_ состояния работоспособности**</dt></span><span class="sxs-lookup"><span data-stu-id="49316-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="49316-120">Состояние работоспособности не найдено; Напажент не имеет кэшированной копии.</span><span class="sxs-lookup"><span data-stu-id="49316-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="49316-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="49316-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="49316-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="49316-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="49316-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="49316-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="49316-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49316-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="49316-125">Требования</span><span class="sxs-lookup"><span data-stu-id="49316-125">Requirements</span></span>



| <span data-ttu-id="49316-126">Требование</span><span class="sxs-lookup"><span data-stu-id="49316-126">Requirement</span></span> | <span data-ttu-id="49316-127">Значение</span><span class="sxs-lookup"><span data-stu-id="49316-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49316-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49316-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49316-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49316-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49316-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49316-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49316-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49316-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49316-132">Header</span><span class="sxs-lookup"><span data-stu-id="49316-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="49316-133"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="49316-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="49316-134">IDL</span><span class="sxs-lookup"><span data-stu-id="49316-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49316-135"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49316-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="49316-136">DLL</span><span class="sxs-lookup"><span data-stu-id="49316-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49316-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49316-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="49316-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49316-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49316-139">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="49316-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





