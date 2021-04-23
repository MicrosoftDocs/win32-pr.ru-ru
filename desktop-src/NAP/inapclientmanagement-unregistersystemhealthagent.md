---
title: Метод Инапклиентманажемент Унрегистерсистемхеалсажент (Напманажемент. h)
description: Отменяет регистрацию SHA в системе защиты доступа к сети.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Метод Унрегистерсистемхеалсажент NAP
- Метод Унрегистерсистемхеалсажент NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Унрегистерсистемхеалсажент
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672765"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="45911-106">Метод Инапклиентманажемент:: Унрегистерсистемхеалсажент</span><span class="sxs-lookup"><span data-stu-id="45911-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="45911-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="45911-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="45911-108">Метод **унрегистерсистемхеалсажент** отменяет регистрацию SHA в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="45911-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="45911-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45911-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="45911-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="45911-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45911-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="45911-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45911-112">Объект [**системхеалсентитид**](nap-datatypes.md) , определяющий отмену регистрации агента работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="45911-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45911-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45911-113">Return value</span></span>

<span data-ttu-id="45911-114">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="45911-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="45911-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="45911-115">Return code</span></span>                                                                                         | <span data-ttu-id="45911-116">Описание</span><span class="sxs-lookup"><span data-stu-id="45911-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="45911-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="45911-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="45911-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="45911-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="45911-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="45911-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="45911-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="45911-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="45911-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45911-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="45911-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45911-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="45911-123"><dt>**\_ \_ по-прежнему \_ привязанный к NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="45911-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="45911-124">SHA остается привязанным и не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="45911-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="45911-125">Требования</span><span class="sxs-lookup"><span data-stu-id="45911-125">Requirements</span></span>



| <span data-ttu-id="45911-126">Требование</span><span class="sxs-lookup"><span data-stu-id="45911-126">Requirement</span></span> | <span data-ttu-id="45911-127">Значение</span><span class="sxs-lookup"><span data-stu-id="45911-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45911-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45911-128">Minimum supported client</span></span><br/> | <span data-ttu-id="45911-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45911-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="45911-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45911-130">Minimum supported server</span></span><br/> | <span data-ttu-id="45911-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45911-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="45911-132">Header</span><span class="sxs-lookup"><span data-stu-id="45911-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="45911-133"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="45911-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="45911-134">IDL</span><span class="sxs-lookup"><span data-stu-id="45911-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45911-135"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45911-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="45911-136">DLL</span><span class="sxs-lookup"><span data-stu-id="45911-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45911-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45911-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="45911-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45911-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45911-139">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="45911-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





