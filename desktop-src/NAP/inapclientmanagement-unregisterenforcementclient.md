---
title: Метод Инапклиентманажемент Унрегистеренфорцементклиент (Напманажемент. h)
description: Отменяет регистрацию клиента принудительного применения в системе защиты доступа к сети.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Метод Унрегистеренфорцементклиент NAP
- Метод Унрегистеренфорцементклиент NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Унрегистеренфорцементклиент
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136574"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="c9acb-106">Метод Инапклиентманажемент:: Унрегистеренфорцементклиент</span><span class="sxs-lookup"><span data-stu-id="c9acb-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="c9acb-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="c9acb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c9acb-108">Метод **унрегистеренфорцементклиент** отменяет регистрацию клиента принудительного применения в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="c9acb-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9acb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9acb-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="c9acb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9acb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9acb-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c9acb-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9acb-112">Значение [**енфорцементентитид**](nap-datatypes.md) , идентифицирующее клиент принудительного применения для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="c9acb-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9acb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9acb-113">Return value</span></span>

<span data-ttu-id="c9acb-114">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="c9acb-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="c9acb-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9acb-115">Return code</span></span>                                                                                         | <span data-ttu-id="c9acb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c9acb-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9acb-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c9acb-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c9acb-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c9acb-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="c9acb-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="c9acb-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c9acb-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="c9acb-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9acb-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="c9acb-123"><dt>**\_ \_ по-прежнему \_ привязанный к NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="c9acb-124">Не удалось отменить регистрацию клиента принудительного применения и он останется привязанным.</span><span class="sxs-lookup"><span data-stu-id="c9acb-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9acb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c9acb-125">Requirements</span></span>



| <span data-ttu-id="c9acb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c9acb-126">Requirement</span></span> | <span data-ttu-id="c9acb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c9acb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9acb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9acb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c9acb-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9acb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c9acb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9acb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c9acb-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9acb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c9acb-132">Header</span><span class="sxs-lookup"><span data-stu-id="c9acb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9acb-133"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9acb-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c9acb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9acb-135"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9acb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c9acb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9acb-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9acb-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="c9acb-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9acb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9acb-139">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="c9acb-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





