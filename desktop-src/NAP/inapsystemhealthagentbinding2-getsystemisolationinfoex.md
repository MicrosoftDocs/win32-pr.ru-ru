---
title: Метод INapSystemHealthAgentBinding2 Жетсистемисолатионинфоекс (Напсистемхеалсажент. h)
description: Вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Метод Жетсистемисолатионинфоекс NAP
- Метод Жетсистемисолатионинфоекс NAP, интерфейс INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 интерфейса NAP, метод Жетсистемисолатионинфоекс
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534319"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="b0d8d-106">Метод INapSystemHealthAgentBinding2:: Жетсистемисолатионинфоекс</span><span class="sxs-lookup"><span data-stu-id="b0d8d-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="b0d8d-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b0d8d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b0d8d-108">Метод **INapSystemHealthAgentBinding2:: жетсистемисолатионинфоекс** вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="b0d8d-109">Используйте [**инапсистемхеалсажентбиндинг:: жетсистемисолатионинфо**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) , чтобы определить только состояние изоляции системы.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b0d8d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0d8d-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="b0d8d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0d8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d8d-112">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0d8d-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d8d-113">Указатель на указатель на структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , содержащий Расширенное состояние изоляции системы для известных соединений.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="b0d8d-114">*исолатионинфо* указывает, находится ли система в состоянии ограниченного доступа, надзор или неограниченный доступ, а также информации [**екстендедисолатионстате**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .</span><span class="sxs-lookup"><span data-stu-id="b0d8d-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="b0d8d-115">*ункновнконнектионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0d8d-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d8d-116">Указатель на **логическое** значение, равное **true** , если какие-либо соединения находятся в неизвестном состоянии, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d8d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0d8d-117">Return value</span></span>

<span data-ttu-id="b0d8d-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b0d8d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0d8d-119">Return code</span></span>                                                                                             | <span data-ttu-id="b0d8d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b0d8d-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0d8d-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="b0d8d-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b0d8d-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="b0d8d-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="b0d8d-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="b0d8d-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="b0d8d-127"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="b0d8d-128">SHA не был инициализирован ранее.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="b0d8d-129"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="b0d8d-130">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="b0d8d-131">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="b0d8d-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0d8d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0d8d-132">Remarks</span></span>

<span data-ttu-id="b0d8d-133">SHA должен освободить структуру [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) , вызвав [**фриисолатионинфоекс**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="b0d8d-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="b0d8d-134">SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0d8d-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d8d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b0d8d-135">Requirements</span></span>



| <span data-ttu-id="b0d8d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b0d8d-136">Requirement</span></span> | <span data-ttu-id="b0d8d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d8d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d8d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0d8d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d8d-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0d8d-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0d8d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0d8d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d8d-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0d8d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0d8d-142">Header</span><span class="sxs-lookup"><span data-stu-id="b0d8d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0d8d-143"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0d8d-144">IDL</span><span class="sxs-lookup"><span data-stu-id="b0d8d-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0d8d-145"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0d8d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b0d8d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0d8d-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0d8d-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b0d8d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0d8d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d8d-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="b0d8d-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





