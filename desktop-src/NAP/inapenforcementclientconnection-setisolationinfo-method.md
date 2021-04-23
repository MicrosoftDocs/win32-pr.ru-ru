---
title: Метод Инапенфорцементклиентконнектион Сетисолатионинфо (Напенфорцементклиент. h)
description: Используется Напажент для установки сведений о изоляции клиента.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Метод Сетисолатионинфо NAP
- Метод Сетисолатионинфо NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетисолатионинфо
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801846"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="692a9-106">Метод Инапенфорцементклиентконнектион:: Сетисолатионинфо</span><span class="sxs-lookup"><span data-stu-id="692a9-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="692a9-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="692a9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="692a9-108">Метод **инапенфорцементклиентконнектион:: сетисолатионинфо** используется напажент для установки сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="692a9-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="692a9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="692a9-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="692a9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="692a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692a9-111">*исолатионинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="692a9-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="692a9-112">Указатель на структуру [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) , которая содержит состояние подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="692a9-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692a9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="692a9-113">Return value</span></span>

<span data-ttu-id="692a9-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="692a9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="692a9-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="692a9-115">Return code</span></span>                                                                                     | <span data-ttu-id="692a9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="692a9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="692a9-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="692a9-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="692a9-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="692a9-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="692a9-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="692a9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="692a9-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="692a9-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="692a9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="692a9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="692a9-123">Remarks</span></span>

<span data-ttu-id="692a9-124">Эта информация задается Напажент после обработки Сохреспонсе и не может быть задана в принудительном применении.</span><span class="sxs-lookup"><span data-stu-id="692a9-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="692a9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="692a9-125">Requirements</span></span>



| <span data-ttu-id="692a9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="692a9-126">Requirement</span></span> | <span data-ttu-id="692a9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="692a9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="692a9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="692a9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="692a9-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="692a9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="692a9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="692a9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="692a9-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="692a9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="692a9-132">Header</span><span class="sxs-lookup"><span data-stu-id="692a9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="692a9-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="692a9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="692a9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="692a9-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="692a9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="692a9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="692a9-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="692a9-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="692a9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="692a9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692a9-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="692a9-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





