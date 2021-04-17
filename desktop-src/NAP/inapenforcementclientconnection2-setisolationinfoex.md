---
title: Метод INapEnforcementClientConnection2 Сетисолатионинфоекс (Напенфорцементклиент. h)
description: Используется Напажент для установки сведений о изоляции клиента.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Метод Сетисолатионинфоекс NAP
- Метод Сетисолатионинфоекс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Сетисолатионинфоекс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672925"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a><span data-ttu-id="56688-106">Метод INapEnforcementClientConnection2:: Сетисолатионинфоекс</span><span class="sxs-lookup"><span data-stu-id="56688-106">INapEnforcementClientConnection2::SetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="56688-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="56688-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="56688-108">Метод **INapEnforcementClientConnection2:: сетисолатионинфоекс** используется напажент для установки сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="56688-108">The **INapEnforcementClientConnection2::SetIsolationInfoEx** method is used by the NapAgent to set the isolation information for the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="56688-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56688-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="56688-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="56688-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56688-111">*исолатионинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56688-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56688-112">Указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , которая содержит состояние подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="56688-112">A pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56688-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56688-113">Return value</span></span>

<span data-ttu-id="56688-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="56688-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="56688-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="56688-115">Return code</span></span>                                                                                     | <span data-ttu-id="56688-116">Описание</span><span class="sxs-lookup"><span data-stu-id="56688-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="56688-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="56688-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="56688-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="56688-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="56688-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="56688-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="56688-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="56688-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="56688-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="56688-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="56688-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56688-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56688-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56688-123">Remarks</span></span>

<span data-ttu-id="56688-124">Эта информация задается Напажент после обработки [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) и не может быть задана в принудительном применении.</span><span class="sxs-lookup"><span data-stu-id="56688-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="56688-125">Требования</span><span class="sxs-lookup"><span data-stu-id="56688-125">Requirements</span></span>



| <span data-ttu-id="56688-126">Требование</span><span class="sxs-lookup"><span data-stu-id="56688-126">Requirement</span></span> | <span data-ttu-id="56688-127">Значение</span><span class="sxs-lookup"><span data-stu-id="56688-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56688-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56688-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56688-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56688-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56688-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56688-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56688-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56688-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56688-132">Header</span><span class="sxs-lookup"><span data-stu-id="56688-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56688-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="56688-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="56688-134">IDL</span><span class="sxs-lookup"><span data-stu-id="56688-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56688-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56688-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="56688-136">DLL</span><span class="sxs-lookup"><span data-stu-id="56688-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56688-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56688-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="56688-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56688-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56688-139">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="56688-139">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





