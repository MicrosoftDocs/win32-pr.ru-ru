---
title: Метод Инапенфорцементклиентконнектион Жетсохреспонсе (Напенфорцементклиент. h)
description: Возвращает SoH-Response, полученную клиентом принудительного применения.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- Метод Жетсохреспонсе NAP
- Метод Жетсохреспонсе NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетсохреспонсе
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891681"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="e827c-106">Метод Инапенфорцементклиентконнектион:: Жетсохреспонсе</span><span class="sxs-lookup"><span data-stu-id="e827c-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="e827c-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e827c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e827c-108">Метод **инапенфорцементклиентконнектион:: жетсохреспонсе** получает SoH-Response, полученную клиентом принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="e827c-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="e827c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e827c-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="e827c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e827c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e827c-111">*сохреспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e827c-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e827c-112">Указатель на указатель на уникальную структуру [**нетворксохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , которая представляет собой большой двоичный объект непрозрачных данных для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="e827c-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e827c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e827c-113">Return value</span></span>

<span data-ttu-id="e827c-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="e827c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e827c-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e827c-115">Return code</span></span>                                                                                     | <span data-ttu-id="e827c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e827c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e827c-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e827c-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="e827c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e827c-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e827c-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e827c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e827c-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e827c-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e827c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e827c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e827c-123">Remarks</span></span>

<span data-ttu-id="e827c-124">Пакет с нулевым размером байта является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e827c-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="e827c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e827c-125">Requirements</span></span>



| <span data-ttu-id="e827c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e827c-126">Requirement</span></span> | <span data-ttu-id="e827c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e827c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e827c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e827c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e827c-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e827c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e827c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e827c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e827c-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e827c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e827c-132">Header</span><span class="sxs-lookup"><span data-stu-id="e827c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e827c-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e827c-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e827c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e827c-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e827c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e827c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e827c-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e827c-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e827c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e827c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e827c-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="e827c-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





