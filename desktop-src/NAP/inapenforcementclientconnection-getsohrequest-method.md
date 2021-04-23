---
title: Метод Инапенфорцементклиентконнектион Жетсохрекуест (Напенфорцементклиент. h)
description: Возвращает текущий запрос SoH.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Метод Жетсохрекуест NAP
- Метод Жетсохрекуест NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетсохрекуест
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988443"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="0b7fa-106">Метод Инапенфорцементклиентконнектион:: Жетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="0b7fa-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="0b7fa-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0b7fa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0b7fa-108">Метод **инапенфорцементклиентконнектион:: жетсохрекуест** получает текущий запрос SoH.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7fa-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b7fa-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="0b7fa-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b7fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7fa-111">*сохрекуест* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b7fa-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7fa-112">Указатель на указатель на структуру [**нетворксохрекуест**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , который представляет собой большой двоичный объект непрозрачных данных для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7fa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b7fa-113">Return value</span></span>

<span data-ttu-id="0b7fa-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0b7fa-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0b7fa-115">Return code</span></span>                                                                                     | <span data-ttu-id="0b7fa-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0b7fa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b7fa-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0b7fa-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0b7fa-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0b7fa-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0b7fa-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0b7fa-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b7fa-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b7fa-123">Remarks</span></span>

<span data-ttu-id="0b7fa-124">Он задается Напажент и запрашивается принудительно для отправки по сети.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="0b7fa-125">Недопустимый пакет SoH с нулевой длиной байт.</span><span class="sxs-lookup"><span data-stu-id="0b7fa-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7fa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0b7fa-126">Requirements</span></span>



| <span data-ttu-id="0b7fa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0b7fa-127">Requirement</span></span> | <span data-ttu-id="0b7fa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0b7fa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7fa-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b7fa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0b7fa-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b7fa-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0b7fa-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b7fa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0b7fa-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b7fa-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0b7fa-133">Header</span><span class="sxs-lookup"><span data-stu-id="0b7fa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b7fa-134"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b7fa-135">IDL</span><span class="sxs-lookup"><span data-stu-id="0b7fa-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b7fa-136"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0b7fa-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0b7fa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b7fa-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b7fa-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0b7fa-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b7fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7fa-140">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="0b7fa-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





