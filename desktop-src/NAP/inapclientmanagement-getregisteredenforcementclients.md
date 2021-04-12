---
title: Метод Инапклиентманажемент Жетрегистереденфорцементклиентс (Напманажемент. h)
description: Извлекает сведения о зарегистрированных клиентах принудительной установки.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Метод Жетрегистереденфорцементклиентс NAP
- Метод Жетрегистереденфорцементклиентс NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Жетрегистереденфорцементклиентс
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491712"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="7a172-106">Метод Инапклиентманажемент:: Жетрегистереденфорцементклиентс</span><span class="sxs-lookup"><span data-stu-id="7a172-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="7a172-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a172-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a172-108">Метод **жетрегистереденфорцементклиентс** извлекает сведения о зарегистрированных клиентах принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="7a172-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a172-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a172-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="7a172-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a172-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a172-111">*количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a172-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a172-112">Указатель на [**енфорцементентитикаунт**](nap-datatypes.md) , содержащий число зарегистрированных клиентов принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="7a172-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="7a172-113">*принудительные условия* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a172-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a172-114">Указатель на массив структур [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , описывающих зарегистрированные клиенты принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="7a172-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a172-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a172-115">Return value</span></span>

<span data-ttu-id="7a172-116">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="7a172-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="7a172-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a172-117">Return code</span></span>                                                                                         | <span data-ttu-id="7a172-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7a172-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a172-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="7a172-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7a172-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7a172-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="7a172-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7a172-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7a172-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="7a172-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a172-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7a172-125"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7a172-126">Напажент не работает.</span><span class="sxs-lookup"><span data-stu-id="7a172-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="7a172-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7a172-127">Requirements</span></span>



| <span data-ttu-id="7a172-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7a172-128">Requirement</span></span> | <span data-ttu-id="7a172-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7a172-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a172-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a172-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a172-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a172-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a172-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a172-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a172-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a172-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7a172-134">Header</span><span class="sxs-lookup"><span data-stu-id="7a172-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a172-135"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a172-136">IDL</span><span class="sxs-lookup"><span data-stu-id="7a172-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a172-137"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a172-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a172-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a172-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a172-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="7a172-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a172-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a172-141">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="7a172-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





