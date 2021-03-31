---
title: Интерфейс INapSystemHealthAgentBinding2 (Напсистемхеалсажент. h)
description: SHA использует для взаимодействия с Напажент. | Интерфейс INapSystemHealthAgentBinding2 (Напсистемхеалсажент. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 интерфейса NAP
- INapSystemHealthAgentBinding2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352795"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="0d52b-106">Интерфейс INapSystemHealthAgentBinding2</span><span class="sxs-lookup"><span data-stu-id="0d52b-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="0d52b-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d52b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0d52b-108">**INapSystemHealthAgentBinding2** предоставляет методы, которые SHA использует для взаимодействия с напажент.</span><span class="sxs-lookup"><span data-stu-id="0d52b-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="0d52b-109">Этот интерфейс наследует все методы [**инапсистемхеалсажентбиндинг**](inapsystemhealthagentbinding.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="0d52b-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="0d52b-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="0d52b-110">Members</span></span>

<span data-ttu-id="0d52b-111">Интерфейс **INapSystemHealthAgentBinding2** наследует от [**инапсистемхеалсажентбиндинг**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="0d52b-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="0d52b-112">**INapSystemHealthAgentBinding2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d52b-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="0d52b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="0d52b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d52b-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0d52b-114">Methods</span></span>

<span data-ttu-id="0d52b-115">Интерфейс **INapSystemHealthAgentBinding2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0d52b-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="0d52b-116">Метод</span><span class="sxs-lookup"><span data-stu-id="0d52b-116">Method</span></span>                                                                                                                    | <span data-ttu-id="0d52b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0d52b-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d52b-118">**INapSystemHealthAgentBinding2:: Жетсистемисолатионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="0d52b-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="0d52b-119">Вызывается SHA для определения состояния изоляции системы и расширенного состояния изоляции.</span><span class="sxs-lookup"><span data-stu-id="0d52b-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d52b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d52b-120">Remarks</span></span>

<span data-ttu-id="0d52b-121">Все API-интерфейсы в этом интерфейсе будут возвращать **RPC \_ E \_ disconnected** , если напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="0d52b-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="0d52b-122">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="0d52b-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d52b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0d52b-123">Requirements</span></span>



| <span data-ttu-id="0d52b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0d52b-124">Requirement</span></span> | <span data-ttu-id="0d52b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0d52b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d52b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d52b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0d52b-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d52b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0d52b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d52b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0d52b-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d52b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d52b-130">Header</span><span class="sxs-lookup"><span data-stu-id="0d52b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d52b-131"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d52b-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d52b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="0d52b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d52b-133"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d52b-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d52b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0d52b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d52b-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d52b-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0d52b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d52b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d52b-137">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="0d52b-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="0d52b-138">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="0d52b-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0d52b-139">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="0d52b-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





