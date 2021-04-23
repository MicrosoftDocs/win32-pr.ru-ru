---
title: Метод Initialize Инапсистемхеалсажентбиндинг (Напсистемхеалсажент. h)
description: Инициализирует агент работоспособности системы (SHA) и привязывает SHA к службе Напажент.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапсистемхеалсажентбиндинг
- Инапсистемхеалсажентбиндинг интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340390"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="36688-106">Метод Инапсистемхеалсажентбиндинг:: Initialize</span><span class="sxs-lookup"><span data-stu-id="36688-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="36688-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="36688-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="36688-108">Метод **инапсистемхеалсажентбиндинг:: Initialize** инициализирует агент работоспособности системы (SHA) и привязывает SHA к службе напажент.</span><span class="sxs-lookup"><span data-stu-id="36688-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="36688-109">Этот метод должен вызываться перед вызовом любого другого метода в интерфейсе [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="36688-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="36688-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36688-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="36688-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="36688-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36688-112">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="36688-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36688-113">Уникальный [системхеалсентитид](nap-datatypes.md) , СОДЕРЖАЩИЙ идентификатор SHA, привязанный к службе напажент.</span><span class="sxs-lookup"><span data-stu-id="36688-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="36688-114">*обратный вызов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36688-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36688-115">COM-указатель на интерфейс [**инапсистемхеалсаженткаллбакк**](inapsystemhealthagentcallback.md) , используемый напажент для обратного вызова агента работоспособности с уведомлением или процессом.</span><span class="sxs-lookup"><span data-stu-id="36688-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="36688-116">Напажент содержит ссылку на объект, связанный с этим интерфейсом, пока не будет вызвана [**неИнициализация**](inapsystemhealthagentbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="36688-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36688-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36688-117">Return value</span></span>

<span data-ttu-id="36688-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="36688-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="36688-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="36688-119">Return code</span></span>                                                                                                | <span data-ttu-id="36688-120">Описание</span><span class="sxs-lookup"><span data-stu-id="36688-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36688-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="36688-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="36688-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="36688-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="36688-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="36688-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="36688-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="36688-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36688-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="36688-127"><dt>**Ошибка \_ уже \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="36688-128">Если SHA был инициализирован ранее, возвращается эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="36688-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="36688-129"><dt>**Защита доступа к сети \_ E \_ не \_ зарегистрирована**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="36688-130">Если SHA не был зарегистрирован ранее, возвращается эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="36688-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="36688-131"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="36688-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="36688-132">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="36688-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="36688-133">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="36688-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36688-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36688-134">Remarks</span></span>

<span data-ttu-id="36688-135">Напажент не запускает обмен данными о состоянии работоспособности в результате инициализации.</span><span class="sxs-lookup"><span data-stu-id="36688-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="36688-136">Агент работоспособности системы должен вызвать [**нотифисохчанже**](inapsystemhealthagentbinding-notifysohchange-method.md) , чтобы запросить обмен пакетами SoH после инициализации с помощью напажент.</span><span class="sxs-lookup"><span data-stu-id="36688-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="36688-137">Требования</span><span class="sxs-lookup"><span data-stu-id="36688-137">Requirements</span></span>



| <span data-ttu-id="36688-138">Требование</span><span class="sxs-lookup"><span data-stu-id="36688-138">Requirement</span></span> | <span data-ttu-id="36688-139">Значение</span><span class="sxs-lookup"><span data-stu-id="36688-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36688-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36688-140">Minimum supported client</span></span><br/> | <span data-ttu-id="36688-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36688-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36688-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36688-142">Minimum supported server</span></span><br/> | <span data-ttu-id="36688-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36688-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36688-144">Header</span><span class="sxs-lookup"><span data-stu-id="36688-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="36688-145"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="36688-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="36688-146">IDL</span><span class="sxs-lookup"><span data-stu-id="36688-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36688-147"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36688-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="36688-148">DLL</span><span class="sxs-lookup"><span data-stu-id="36688-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36688-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36688-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="36688-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36688-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36688-151">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="36688-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





