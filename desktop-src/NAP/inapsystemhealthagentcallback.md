---
title: Интерфейс Инапсистемхеалсаженткаллбакк (Напсистемхеалсажент. h)
description: Объявляются системой и реализуются модулем записи SHA, поэтому Напажент может взаимодействовать с SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Инапсистемхеалсаженткаллбакк интерфейса NAP
- Инапсистемхеалсаженткаллбакк интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672791"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="6ed83-105">Интерфейс Инапсистемхеалсаженткаллбакк</span><span class="sxs-lookup"><span data-stu-id="6ed83-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="6ed83-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="6ed83-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ed83-107">Интерфейс **инапсистемхеалсаженткаллбакк** предоставляет методы обратного вызова, которые объявляются системой и реализуются модулем записи SHA, поэтому напажент может взаимодействовать с SHA.</span><span class="sxs-lookup"><span data-stu-id="6ed83-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="6ed83-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6ed83-108">Members</span></span>

<span data-ttu-id="6ed83-109">Интерфейс **инапсистемхеалсаженткаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6ed83-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6ed83-110">**Инапсистемхеалсаженткаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ed83-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="6ed83-111">Методы</span><span class="sxs-lookup"><span data-stu-id="6ed83-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ed83-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6ed83-112">Methods</span></span>

<span data-ttu-id="6ed83-113">Интерфейс **инапсистемхеалсаженткаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6ed83-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="6ed83-114">Метод</span><span class="sxs-lookup"><span data-stu-id="6ed83-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="6ed83-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6ed83-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ed83-116">**Инапсистемхеалсаженткаллбакк:: Компаресохрекуестс**</span><span class="sxs-lookup"><span data-stu-id="6ed83-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="6ed83-117">Используется SHA для сравнения SoH.</span><span class="sxs-lookup"><span data-stu-id="6ed83-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="6ed83-118">**Инапсистемхеалсаженткаллбакк:: Жетфиксупинфо**</span><span class="sxs-lookup"><span data-stu-id="6ed83-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="6ed83-119">Вызывается методом Напажент для определения состояния SHA.</span><span class="sxs-lookup"><span data-stu-id="6ed83-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="6ed83-120">**Инапсистемхеалсаженткаллбакк:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="6ed83-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="6ed83-121">Вызывается Напажент для запроса запроса SoH SHA.</span><span class="sxs-lookup"><span data-stu-id="6ed83-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="6ed83-122">**Инапсистемхеалсаженткаллбакк:: Нотифйорфанедсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="6ed83-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="6ed83-123">Вызывается, если запрос SoH был запрошен из SHA, но ответ никогда не был возвращен.</span><span class="sxs-lookup"><span data-stu-id="6ed83-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="6ed83-124">**Инапсистемхеалсаженткаллбакк:: Нотифисистемисолатионстатечанже**</span><span class="sxs-lookup"><span data-stu-id="6ed83-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="6ed83-125">Вызывается Напажент для указания на то, что состояние изоляции системы или время окончания надзора изменилось.</span><span class="sxs-lookup"><span data-stu-id="6ed83-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="6ed83-126">**Инапсистемхеалсаженткаллбакк::P Роцесссохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="6ed83-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="6ed83-127">Вызывается, когда Напажент получает ответ SoH, предназначенный для этого агента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="6ed83-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="6ed83-128">Требования</span><span class="sxs-lookup"><span data-stu-id="6ed83-128">Requirements</span></span>



| <span data-ttu-id="6ed83-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6ed83-129">Requirement</span></span> | <span data-ttu-id="6ed83-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6ed83-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed83-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ed83-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed83-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ed83-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ed83-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ed83-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed83-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ed83-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ed83-135">Header</span><span class="sxs-lookup"><span data-stu-id="6ed83-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed83-136"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed83-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ed83-137">IDL</span><span class="sxs-lookup"><span data-stu-id="6ed83-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ed83-138"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ed83-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed83-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ed83-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed83-140">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="6ed83-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6ed83-141">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="6ed83-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

