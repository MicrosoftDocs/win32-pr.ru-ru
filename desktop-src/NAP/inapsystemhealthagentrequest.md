---
title: Интерфейс Инапсистемхеалсажентрекуест (Напсистемхеалсажент. h)
description: SHA используется для обмена данными и координации обработки с системой защиты доступа к сети.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- Инапсистемхеалсажентрекуест интерфейса NAP
- Инапсистемхеалсажентрекуест интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534091"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="1e245-105">Интерфейс Инапсистемхеалсажентрекуест</span><span class="sxs-lookup"><span data-stu-id="1e245-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="1e245-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="1e245-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1e245-107">Интерфейс **инапсистемхеалсажентрекуест** предоставляет методы, которые SHA использует для обмена данными и координации обработки в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="1e245-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="1e245-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1e245-108">Members</span></span>

<span data-ttu-id="1e245-109">Интерфейс **инапсистемхеалсажентрекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1e245-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e245-110">**Инапсистемхеалсажентрекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1e245-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="1e245-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1e245-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e245-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1e245-112">Methods</span></span>

<span data-ttu-id="1e245-113">Интерфейс **инапсистемхеалсажентрекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1e245-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="1e245-114">Метод</span><span class="sxs-lookup"><span data-stu-id="1e245-114">Method</span></span>                                                                                                                     | <span data-ttu-id="1e245-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1e245-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e245-116">**Инапсистемхеалсажентрекуест:: Жеткачесохфлаг**</span><span class="sxs-lookup"><span data-stu-id="1e245-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="1e245-117">Используется только Напажент.</span><span class="sxs-lookup"><span data-stu-id="1e245-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="1e245-118">**Инапсистемхеалсажентрекуест:: Жеткоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="1e245-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="1e245-119">Используется агентами работоспособности системы для корреляции SoH и [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="1e245-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="1e245-120">**Инапсистемхеалсажентрекуест:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="1e245-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="1e245-121">Используется SHA для получения SoH, ранее кэшированного Напажент.</span><span class="sxs-lookup"><span data-stu-id="1e245-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="1e245-122">**Инапсистемхеалсажентрекуест:: Жетсохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="1e245-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="1e245-123">Используется агентом работоспособности для получения [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="1e245-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="1e245-124">**Инапсистемхеалсажентрекуест:: Жетстрингкоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="1e245-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="1e245-125">Используется агентами работоспособности системы для регистрации идентификатора корреляции.</span><span class="sxs-lookup"><span data-stu-id="1e245-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="1e245-126">**Инапсистемхеалсажентрекуест:: Сетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="1e245-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="1e245-127">Используется агентами работоспособности для записи своего запроса SoH.</span><span class="sxs-lookup"><span data-stu-id="1e245-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="1e245-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1e245-128">Requirements</span></span>



| <span data-ttu-id="1e245-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1e245-129">Requirement</span></span> | <span data-ttu-id="1e245-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1e245-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e245-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e245-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1e245-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e245-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e245-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e245-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1e245-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e245-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e245-135">Header</span><span class="sxs-lookup"><span data-stu-id="1e245-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e245-136"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e245-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e245-137">IDL</span><span class="sxs-lookup"><span data-stu-id="1e245-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e245-138"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e245-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="1e245-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1e245-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e245-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e245-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="1e245-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e245-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e245-142">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="1e245-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1e245-143">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="1e245-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

