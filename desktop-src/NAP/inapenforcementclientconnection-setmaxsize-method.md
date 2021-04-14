---
title: Метод Инапенфорцементклиентконнектион Сетмакссизе (Напенфорцементклиент. h)
description: Задает максимальный размер пакета SoH для этого клиента.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Метод Сетмакссизе NAP
- Метод Сетмакссизе NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетмакссизе
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415261"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="13465-106">Метод Инапенфорцементклиентконнектион:: Сетмакссизе</span><span class="sxs-lookup"><span data-stu-id="13465-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="13465-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="13465-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13465-108">Метод **инапенфорцементклиентконнектион:: сетмакссизе** задает максимальный размер пакета SoH для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="13465-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="13465-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13465-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="13465-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="13465-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13465-111">*MAXSIZE* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13465-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13465-112">Структура [**протоколмакссизе**](nap-datatypes.md) , указывающая максимальный размер пакета SOH (в байтах).</span><span class="sxs-lookup"><span data-stu-id="13465-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13465-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13465-113">Return value</span></span>

<span data-ttu-id="13465-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="13465-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="13465-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="13465-115">Return code</span></span>                                                                                     | <span data-ttu-id="13465-116">Описание</span><span class="sxs-lookup"><span data-stu-id="13465-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13465-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="13465-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="13465-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="13465-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="13465-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="13465-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="13465-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="13465-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="13465-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13465-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="13465-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13465-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13465-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13465-123">Remarks</span></span>

<span data-ttu-id="13465-124">Это значение задается клиентом принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="13465-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="13465-125">Требования</span><span class="sxs-lookup"><span data-stu-id="13465-125">Requirements</span></span>



| <span data-ttu-id="13465-126">Требование</span><span class="sxs-lookup"><span data-stu-id="13465-126">Requirement</span></span> | <span data-ttu-id="13465-127">Значение</span><span class="sxs-lookup"><span data-stu-id="13465-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13465-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13465-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13465-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13465-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13465-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13465-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13465-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13465-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13465-132">Header</span><span class="sxs-lookup"><span data-stu-id="13465-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="13465-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="13465-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="13465-134">IDL</span><span class="sxs-lookup"><span data-stu-id="13465-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13465-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13465-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="13465-136">DLL</span><span class="sxs-lookup"><span data-stu-id="13465-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13465-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13465-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="13465-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13465-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13465-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="13465-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





