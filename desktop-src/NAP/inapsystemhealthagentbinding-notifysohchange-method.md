---
title: Метод Инапсистемхеалсажентбиндинг Нотифисохчанже (Напсистемхеалсажент. h)
description: Используется SHA при изменении состояния работоспособности.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Метод Нотифисохчанже NAP
- Метод Нотифисохчанже NAP, интерфейс Инапсистемхеалсажентбиндинг
- Инапсистемхеалсажентбиндинг интерфейса NAP, метод Нотифисохчанже
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535333"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="770a6-106">Метод Инапсистемхеалсажентбиндинг:: Нотифисохчанже</span><span class="sxs-lookup"><span data-stu-id="770a6-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="770a6-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="770a6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="770a6-108">Метод **инапсистемхеалсажентбиндинг:: нотифисохчанже** используется SHA при изменении состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="770a6-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="770a6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="770a6-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="770a6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="770a6-110">Parameters</span></span>

<span data-ttu-id="770a6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="770a6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="770a6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="770a6-112">Return value</span></span>

<span data-ttu-id="770a6-113">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="770a6-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="770a6-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="770a6-114">Return code</span></span>                                                                                             | <span data-ttu-id="770a6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="770a6-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="770a6-116"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="770a6-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="770a6-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="770a6-118"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="770a6-119">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="770a6-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="770a6-120"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="770a6-121">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="770a6-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="770a6-122"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="770a6-123">SHA не был инициализирован ранее.</span><span class="sxs-lookup"><span data-stu-id="770a6-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="770a6-124"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="770a6-125">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="770a6-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="770a6-126">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="770a6-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="770a6-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="770a6-127">Remarks</span></span>

<span data-ttu-id="770a6-128">SHA не должен явно вызывать этот API, так как он приводит к обмену данными о состоянии работоспособности по сети.</span><span class="sxs-lookup"><span data-stu-id="770a6-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="770a6-129">Вызовы этого API должны выполняться только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="770a6-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="770a6-130">Напажент не удерживает этот поток для обработки изменения состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="770a6-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="770a6-131">Вместо этого он немедленно возвращает значение и обрабатывает изменения асинхронно.</span><span class="sxs-lookup"><span data-stu-id="770a6-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="770a6-132">SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="770a6-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="770a6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="770a6-133">Requirements</span></span>



| <span data-ttu-id="770a6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="770a6-134">Requirement</span></span> | <span data-ttu-id="770a6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="770a6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="770a6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="770a6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="770a6-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="770a6-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="770a6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="770a6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="770a6-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="770a6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="770a6-140">Header</span><span class="sxs-lookup"><span data-stu-id="770a6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="770a6-141"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="770a6-142">IDL</span><span class="sxs-lookup"><span data-stu-id="770a6-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="770a6-143"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="770a6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="770a6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="770a6-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="770a6-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="770a6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="770a6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770a6-147">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="770a6-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





