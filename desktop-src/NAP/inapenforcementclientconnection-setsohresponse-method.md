---
title: Метод Инапенфорцементклиентконнектион Сетсохреспонсе (Напенфорцементклиент. h)
description: Задает SoH-Response и используется клиентом принудительного применения при получении пакета.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Метод Сетсохреспонсе NAP
- Метод Сетсохреспонсе NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетсохреспонсе
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491925"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="17161-106">Метод Инапенфорцементклиентконнектион:: Сетсохреспонсе</span><span class="sxs-lookup"><span data-stu-id="17161-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="17161-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="17161-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="17161-108">Метод **инапенфорцементклиентконнектион:: сетсохреспонсе** задает SoH-Response и используется клиентом принудительного применения при получении пакета.</span><span class="sxs-lookup"><span data-stu-id="17161-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="17161-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17161-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="17161-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="17161-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17161-111">*сохреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17161-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17161-112">Указатель на уникальную структуру [**нетворксохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , которая представляет собой большой двоичный объект непрозрачных данных для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="17161-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17161-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17161-113">Return value</span></span>

<span data-ttu-id="17161-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="17161-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="17161-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="17161-115">Return code</span></span>                                                                                     | <span data-ttu-id="17161-116">Описание</span><span class="sxs-lookup"><span data-stu-id="17161-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="17161-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="17161-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="17161-118">Пакет SoH является допустимым.</span><span class="sxs-lookup"><span data-stu-id="17161-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="17161-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="17161-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="17161-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="17161-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="17161-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17161-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="17161-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17161-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17161-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17161-123">Remarks</span></span>

<span data-ttu-id="17161-124">Пакет нулевого размера является допустимым.</span><span class="sxs-lookup"><span data-stu-id="17161-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="17161-125">Требования</span><span class="sxs-lookup"><span data-stu-id="17161-125">Requirements</span></span>



| <span data-ttu-id="17161-126">Требование</span><span class="sxs-lookup"><span data-stu-id="17161-126">Requirement</span></span> | <span data-ttu-id="17161-127">Значение</span><span class="sxs-lookup"><span data-stu-id="17161-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17161-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17161-128">Minimum supported client</span></span><br/> | <span data-ttu-id="17161-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17161-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="17161-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17161-130">Minimum supported server</span></span><br/> | <span data-ttu-id="17161-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17161-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="17161-132">Header</span><span class="sxs-lookup"><span data-stu-id="17161-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="17161-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="17161-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="17161-134">IDL</span><span class="sxs-lookup"><span data-stu-id="17161-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17161-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17161-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="17161-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17161-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17161-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17161-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="17161-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17161-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17161-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="17161-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





