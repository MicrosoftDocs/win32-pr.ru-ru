---
title: Метод Инапенфорцементклиентконнектион Жетисолатионинфо (Напенфорцементклиент. h)
description: Используется для получения сведений о изоляции клиента.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Метод Жетисолатионинфо NAP
- Метод Жетисолатионинфо NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетисолатионинфо
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989397"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="a3e08-106">Метод Инапенфорцементклиентконнектион:: Жетисолатионинфо</span><span class="sxs-lookup"><span data-stu-id="a3e08-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="a3e08-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="a3e08-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a3e08-108">Метод **инапенфорцементклиентконнектион:: жетисолатионинфо** используется для получения сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="a3e08-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e08-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3e08-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a3e08-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3e08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e08-111">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a3e08-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e08-112">Указатель на указатель на структуру [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) , которая содержит состояние подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="a3e08-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e08-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3e08-113">Return value</span></span>

<span data-ttu-id="a3e08-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="a3e08-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a3e08-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a3e08-115">Return code</span></span>                                                                                     | <span data-ttu-id="a3e08-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e08-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3e08-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a3e08-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="a3e08-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a3e08-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a3e08-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="a3e08-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a3e08-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a3e08-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3e08-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3e08-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3e08-123">Remarks</span></span>

<span data-ttu-id="a3e08-124">Эта информация задается Напажент после обработки [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) и не может быть задана с помощью принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="a3e08-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e08-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a3e08-125">Requirements</span></span>



| <span data-ttu-id="a3e08-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a3e08-126">Requirement</span></span> | <span data-ttu-id="a3e08-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a3e08-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e08-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3e08-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e08-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3e08-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3e08-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3e08-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e08-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3e08-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3e08-132">Header</span><span class="sxs-lookup"><span data-stu-id="a3e08-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e08-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3e08-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a3e08-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3e08-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a3e08-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e08-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e08-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e08-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a3e08-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3e08-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e08-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="a3e08-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





