---
title: Метод INapEnforcementClientConnection2 Жетисолатионинфоекс (Напенфорцементклиент. h)
description: Используется для получения сведений о изоляции клиента.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Метод Жетисолатионинфоекс NAP
- Метод Жетисолатионинфоекс NAP, интерфейс INapEnforcementClientConnection2
- INapEnforcementClientConnection2 интерфейса NAP, метод Жетисолатионинфоекс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493239"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="cf713-106">Метод INapEnforcementClientConnection2:: Жетисолатионинфоекс</span><span class="sxs-lookup"><span data-stu-id="cf713-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="cf713-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="cf713-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cf713-108">Метод **INapEnforcementClientConnection2:: жетисолатионинфоекс** используется для получения сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="cf713-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf713-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf713-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="cf713-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf713-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf713-111">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf713-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf713-112">Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , которая содержит подключение и расширенные сведения о состоянии клиента.</span><span class="sxs-lookup"><span data-stu-id="cf713-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf713-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf713-113">Return value</span></span>

<span data-ttu-id="cf713-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="cf713-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cf713-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cf713-115">Return code</span></span>                                                                                     | <span data-ttu-id="cf713-116">Описание</span><span class="sxs-lookup"><span data-stu-id="cf713-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf713-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cf713-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="cf713-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cf713-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cf713-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="cf713-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cf713-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cf713-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf713-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf713-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf713-123">Remarks</span></span>

<span data-ttu-id="cf713-124">Эта информация задается Напажент после обработки [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) и не может быть задана в принудительном применении.</span><span class="sxs-lookup"><span data-stu-id="cf713-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="cf713-125">SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="cf713-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf713-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cf713-126">Requirements</span></span>



| <span data-ttu-id="cf713-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cf713-127">Requirement</span></span> | <span data-ttu-id="cf713-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cf713-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf713-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf713-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf713-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf713-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf713-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf713-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf713-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf713-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf713-133">Header</span><span class="sxs-lookup"><span data-stu-id="cf713-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf713-134"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf713-135">IDL</span><span class="sxs-lookup"><span data-stu-id="cf713-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf713-136"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="cf713-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf713-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf713-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf713-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cf713-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf713-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf713-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="cf713-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





