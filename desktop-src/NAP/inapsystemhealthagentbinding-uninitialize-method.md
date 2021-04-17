---
title: Метод Uninitialize Инапсистемхеалсажентбиндинг (Напсистемхеалсажент. h)
description: Заставляет Напажент освобождать все ссылки на указатели COM агента работоспособности системы.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Отмена инициализации метода NAP
- Отмена инициализации метода NAP, интерфейс Инапсистемхеалсажентбиндинг
- Инапсистемхеалсажентбиндинг интерфейс NAP, метод Uninitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672697"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="4a903-106">Метод Инапсистемхеалсажентбиндинг:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="4a903-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="4a903-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4a903-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4a903-108">Метод **инапсистемхеалсажентбиндинг:: Uninitialize** приводит к тому, что напажент освобождает все свои ссылки на указатели COM агента работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="4a903-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a903-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a903-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="4a903-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a903-110">Parameters</span></span>

<span data-ttu-id="4a903-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4a903-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a903-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a903-112">Return value</span></span>

<span data-ttu-id="4a903-113">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="4a903-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4a903-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4a903-114">Return code</span></span>                                                                                             | <span data-ttu-id="4a903-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4a903-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a903-116"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="4a903-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="4a903-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="4a903-118"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="4a903-119">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4a903-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="4a903-120"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="4a903-121">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a903-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="4a903-122"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="4a903-123">SHA не был инициализирован ранее.</span><span class="sxs-lookup"><span data-stu-id="4a903-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="4a903-124"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="4a903-125">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="4a903-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="4a903-126">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="4a903-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a903-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a903-127">Remarks</span></span>

<span data-ttu-id="4a903-128">Напажент блокирует выполнение этого вызова метода до завершения всех существующих вызовов в интерфейсах привязки и обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4a903-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="4a903-129">SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="4a903-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a903-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4a903-130">Requirements</span></span>



| <span data-ttu-id="4a903-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4a903-131">Requirement</span></span> | <span data-ttu-id="4a903-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4a903-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a903-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a903-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4a903-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a903-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a903-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a903-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4a903-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a903-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a903-137">Header</span><span class="sxs-lookup"><span data-stu-id="4a903-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a903-138"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a903-139">IDL</span><span class="sxs-lookup"><span data-stu-id="4a903-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a903-140"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a903-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4a903-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a903-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a903-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4a903-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a903-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a903-144">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="4a903-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





