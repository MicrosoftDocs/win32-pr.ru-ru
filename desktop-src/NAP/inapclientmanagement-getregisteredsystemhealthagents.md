---
title: Метод Инапклиентманажемент Жетрегистередсистемхеалсажентс (Напманажемент. h)
description: Извлекает сведения о зарегистрированном SHA.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Метод Жетрегистередсистемхеалсажентс NAP
- Метод Жетрегистередсистемхеалсажентс NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Жетрегистередсистемхеалсажентс
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988957"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="95b33-106">Метод Инапклиентманажемент:: Жетрегистередсистемхеалсажентс</span><span class="sxs-lookup"><span data-stu-id="95b33-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="95b33-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="95b33-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="95b33-108">Метод **жетрегистередсистемхеалсажентс** извлекает сведения о зарегистрированных SHA.</span><span class="sxs-lookup"><span data-stu-id="95b33-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b33-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95b33-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="95b33-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="95b33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b33-111">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95b33-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b33-112">Указатель на [**системхеалсентитикаунт**](nap-datatypes.md) , описывающий число зарегистрированных SHA.</span><span class="sxs-lookup"><span data-stu-id="95b33-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="95b33-113">*агенты* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95b33-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b33-114">Указатель на массив структур [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , описывающих зарегистрированный SHA.</span><span class="sxs-lookup"><span data-stu-id="95b33-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b33-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95b33-115">Return value</span></span>

<span data-ttu-id="95b33-116">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="95b33-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="95b33-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="95b33-117">Return code</span></span>                                                                                         | <span data-ttu-id="95b33-118">Описание</span><span class="sxs-lookup"><span data-stu-id="95b33-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="95b33-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="95b33-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="95b33-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="95b33-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="95b33-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="95b33-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="95b33-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="95b33-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95b33-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="95b33-125"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="95b33-126">Напажент не работает.</span><span class="sxs-lookup"><span data-stu-id="95b33-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="95b33-127">Требования</span><span class="sxs-lookup"><span data-stu-id="95b33-127">Requirements</span></span>



| <span data-ttu-id="95b33-128">Требование</span><span class="sxs-lookup"><span data-stu-id="95b33-128">Requirement</span></span> | <span data-ttu-id="95b33-129">Значение</span><span class="sxs-lookup"><span data-stu-id="95b33-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b33-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95b33-130">Minimum supported client</span></span><br/> | <span data-ttu-id="95b33-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95b33-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="95b33-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95b33-132">Minimum supported server</span></span><br/> | <span data-ttu-id="95b33-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95b33-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95b33-134">Header</span><span class="sxs-lookup"><span data-stu-id="95b33-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b33-135"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="95b33-136">IDL</span><span class="sxs-lookup"><span data-stu-id="95b33-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95b33-137"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="95b33-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95b33-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b33-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b33-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="95b33-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95b33-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b33-141">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="95b33-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





