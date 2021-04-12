---
title: Метод Инапсистемхеалсажентбиндинг Жетсистемисолатионинфо (Напсистемхеалсажент. h)
description: Вызывается SHA для определения состояния изоляции системы.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Метод Жетсистемисолатионинфо NAP
- Метод Жетсистемисолатионинфо NAP, интерфейс Инапсистемхеалсажентбиндинг
- Инапсистемхеалсажентбиндинг интерфейса NAP, метод Жетсистемисолатионинфо
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492939"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="3cfa8-106">Метод Инапсистемхеалсажентбиндинг:: Жетсистемисолатионинфо</span><span class="sxs-lookup"><span data-stu-id="3cfa8-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="3cfa8-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="3cfa8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3cfa8-108">Метод **инапсистемхеалсажентбиндинг:: жетсистемисолатионинфо** вызывается SHA для определения состояния изоляции системы.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="3cfa8-109">Используйте [**INapSystemHealthAgentBinding2:: жетсистемисолатионинфоекс**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) , чтобы определить Расширенное состояние изоляции системы.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3cfa8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cfa8-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="3cfa8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cfa8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cfa8-112">*исолатионинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa8-113">Указатель на указатель на структуру [**исолатионинфо**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) , который содержит состояние изоляции системы для известных соединений.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="3cfa8-114">*исолатионинфоиндикатес* , если система находится в состоянии ограниченного доступа, надзора или неограниченного доступа.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="3cfa8-115">*ункновнконнектионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfa8-116">Указатель на **логическое** значение, равное **true** , если какие-либо соединения находятся в неизвестном состоянии, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cfa8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cfa8-117">Return value</span></span>

<span data-ttu-id="3cfa8-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3cfa8-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3cfa8-119">Return code</span></span>                                                                                             | <span data-ttu-id="3cfa8-120">Описание</span><span class="sxs-lookup"><span data-stu-id="3cfa8-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3cfa8-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="3cfa8-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="3cfa8-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="3cfa8-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="3cfa8-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="3cfa8-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="3cfa8-127"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="3cfa8-128">SHA не был инициализирован ранее.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="3cfa8-129"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="3cfa8-130">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="3cfa8-131">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="3cfa8-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3cfa8-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cfa8-132">Remarks</span></span>

<span data-ttu-id="3cfa8-133">SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfa8-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cfa8-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3cfa8-134">Requirements</span></span>



| <span data-ttu-id="3cfa8-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3cfa8-135">Requirement</span></span> | <span data-ttu-id="3cfa8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3cfa8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfa8-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cfa8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfa8-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3cfa8-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cfa8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfa8-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3cfa8-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3cfa8-141">Header</span><span class="sxs-lookup"><span data-stu-id="3cfa8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cfa8-142"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cfa8-143">IDL</span><span class="sxs-lookup"><span data-stu-id="3cfa8-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3cfa8-144"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="3cfa8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3cfa8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cfa8-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa8-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3cfa8-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cfa8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfa8-148">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="3cfa8-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





