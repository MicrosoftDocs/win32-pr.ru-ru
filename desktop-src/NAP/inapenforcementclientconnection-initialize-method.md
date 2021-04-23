---
title: Метод Initialize Инапенфорцементклиентконнектион (Напенфорцементклиент. h)
description: Инициализирует клиентское соединение.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489885"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="15cb6-106">Метод Инапенфорцементклиентконнектион:: Initialize</span><span class="sxs-lookup"><span data-stu-id="15cb6-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="15cb6-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="15cb6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="15cb6-108">Метод **инапенфорцементклиентконнектион:: Initialize** инициализирует клиентское соединение.</span><span class="sxs-lookup"><span data-stu-id="15cb6-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cb6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15cb6-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="15cb6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="15cb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15cb6-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="15cb6-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15cb6-112">Указатель на объект [**енфорементентитид**](nap-datatypes.md) , который идентифицирует клиент принудительного применения, запрашивающий соединение.</span><span class="sxs-lookup"><span data-stu-id="15cb6-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="15cb6-113">Это значение задается Напажент во время создания соединения.</span><span class="sxs-lookup"><span data-stu-id="15cb6-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15cb6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15cb6-114">Return value</span></span>

<span data-ttu-id="15cb6-115">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="15cb6-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="15cb6-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15cb6-116">Return code</span></span>                                                                                     | <span data-ttu-id="15cb6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="15cb6-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="15cb6-118"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="15cb6-119">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="15cb6-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="15cb6-120"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="15cb6-121">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="15cb6-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="15cb6-122"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="15cb6-123">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15cb6-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15cb6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="15cb6-124">Requirements</span></span>



| <span data-ttu-id="15cb6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="15cb6-125">Requirement</span></span> | <span data-ttu-id="15cb6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="15cb6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15cb6-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15cb6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15cb6-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15cb6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15cb6-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15cb6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15cb6-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15cb6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15cb6-131">Header</span><span class="sxs-lookup"><span data-stu-id="15cb6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="15cb6-132"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="15cb6-133">IDL</span><span class="sxs-lookup"><span data-stu-id="15cb6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15cb6-134"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="15cb6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="15cb6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15cb6-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15cb6-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="15cb6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15cb6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cb6-138">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="15cb6-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





