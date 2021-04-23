---
title: Метод Инапенфорцементклиентконнектион Сетсохрекуест (Напенфорцементклиент. h)
description: Задает запрос SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Метод Сетсохрекуест NAP
- Метод Сетсохрекуест NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетсохрекуест
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801834"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="11f35-106">Метод Инапенфорцементклиентконнектион:: Сетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="11f35-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="11f35-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="11f35-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="11f35-108">Метод **инапенфорцементклиентконнектион:: сетсохрекуест** задает запрос SoH.</span><span class="sxs-lookup"><span data-stu-id="11f35-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f35-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f35-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="11f35-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="11f35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f35-111">*сохрекуест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11f35-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f35-112">Указатель на уникальную структуру [**нетворксохрекуест**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , которая представляет собой большой двоичный объект непрозрачных данных для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="11f35-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f35-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11f35-113">Return value</span></span>

<span data-ttu-id="11f35-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="11f35-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="11f35-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="11f35-115">Return code</span></span>                                                                                     | <span data-ttu-id="11f35-116">Описание</span><span class="sxs-lookup"><span data-stu-id="11f35-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="11f35-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="11f35-118">Пакет SoH является допустимым.</span><span class="sxs-lookup"><span data-stu-id="11f35-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="11f35-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="11f35-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="11f35-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="11f35-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="11f35-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11f35-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11f35-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11f35-123">Remarks</span></span>

<span data-ttu-id="11f35-124">Он задается Напажент и запрашивается принудительно для отправки по сети.</span><span class="sxs-lookup"><span data-stu-id="11f35-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="11f35-125">Недопустимый пакет SoH с нулевой длиной байт.</span><span class="sxs-lookup"><span data-stu-id="11f35-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f35-126">Требования</span><span class="sxs-lookup"><span data-stu-id="11f35-126">Requirements</span></span>



| <span data-ttu-id="11f35-127">Требование</span><span class="sxs-lookup"><span data-stu-id="11f35-127">Requirement</span></span> | <span data-ttu-id="11f35-128">Значение</span><span class="sxs-lookup"><span data-stu-id="11f35-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f35-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11f35-129">Minimum supported client</span></span><br/> | <span data-ttu-id="11f35-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11f35-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11f35-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11f35-131">Minimum supported server</span></span><br/> | <span data-ttu-id="11f35-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11f35-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11f35-133">Header</span><span class="sxs-lookup"><span data-stu-id="11f35-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f35-134"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="11f35-135">IDL</span><span class="sxs-lookup"><span data-stu-id="11f35-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11f35-136"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="11f35-137">DLL</span><span class="sxs-lookup"><span data-stu-id="11f35-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f35-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f35-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="11f35-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f35-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f35-140">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="11f35-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





