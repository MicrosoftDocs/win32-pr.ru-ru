---
title: Интерфейс INapComponentConfig2 (Напкоммон. h)
description: Предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для удаленной настройки пользовательского интерфейса сервера сетевых политик (NPS).
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2 интерфейса NAP
- INapComponentConfig2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661861"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="8bb57-105">Интерфейс INapComponentConfig2</span><span class="sxs-lookup"><span data-stu-id="8bb57-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="8bb57-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="8bb57-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8bb57-107">Интерфейс **INapComponentConfig2** предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для удаленной настройки пользовательского интерфейса сервера политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="8bb57-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="8bb57-108">Этот интерфейс наследует все методы [**инапкомпонентконфиг**](inapcomponentconfig.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="8bb57-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="8bb57-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="8bb57-109">Members</span></span>

<span data-ttu-id="8bb57-110">Интерфейс **INapComponentConfig2** наследует от [**инапкомпонентконфиг**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="8bb57-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="8bb57-111">**INapComponentConfig2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8bb57-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="8bb57-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8bb57-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8bb57-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8bb57-113">Methods</span></span>

<span data-ttu-id="8bb57-114">Интерфейс **INapComponentConfig2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8bb57-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="8bb57-115">Метод</span><span class="sxs-lookup"><span data-stu-id="8bb57-115">Method</span></span>                                                                                                | <span data-ttu-id="8bb57-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8bb57-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb57-117">**INapComponentConfig2:: Инвокеуиформачине**</span><span class="sxs-lookup"><span data-stu-id="8bb57-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="8bb57-118">Реализуется средствами SHV по мере необходимости для управления удаленной конфигурацией непосредственно на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8bb57-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="8bb57-119">**INapComponentConfig2:: Инвокеуифромконфигблоб**</span><span class="sxs-lookup"><span data-stu-id="8bb57-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="8bb57-120">Реализуется средствами SHV по мере необходимости для загрузки конфигурации удаленного компьютера в памяти и вывода пользовательского интерфейса, позволяющего манипулировать данными конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8bb57-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="8bb57-121">**INapComponentConfig2:: Исремотеконфигсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8bb57-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="8bb57-122">Реализуется средствами SHV, чтобы указать, поддерживается ли удаленная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="8bb57-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="8bb57-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bb57-123">Remarks</span></span>

<span data-ttu-id="8bb57-124">Этот интерфейс не должен реализовываться агентами работоспособности системы (SHA) или клиентами принудительного применения карантина (кекс).</span><span class="sxs-lookup"><span data-stu-id="8bb57-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb57-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8bb57-125">Requirements</span></span>



| <span data-ttu-id="8bb57-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8bb57-126">Requirement</span></span> | <span data-ttu-id="8bb57-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8bb57-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb57-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bb57-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb57-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8bb57-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8bb57-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bb57-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb57-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8bb57-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8bb57-132">Header</span><span class="sxs-lookup"><span data-stu-id="8bb57-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb57-133"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb57-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bb57-134">IDL</span><span class="sxs-lookup"><span data-stu-id="8bb57-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bb57-135"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bb57-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb57-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bb57-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb57-137">**инапкомпонентконфиг**</span><span class="sxs-lookup"><span data-stu-id="8bb57-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="8bb57-138">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="8bb57-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8bb57-139">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="8bb57-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





