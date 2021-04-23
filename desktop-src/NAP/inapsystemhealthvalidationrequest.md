---
title: Интерфейс Инапсистемхеалсвалидатионрекуест (Напсистемхеалсвалидатор. h)
description: Используются для поддержки средств проверки работоспособности системы, которые определяются разработчиком приложения.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- Инапсистемхеалсвалидатионрекуест интерфейса NAP
- Инапсистемхеалсвалидатионрекуест интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803802"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="4907a-105">Интерфейс Инапсистемхеалсвалидатионрекуест</span><span class="sxs-lookup"><span data-stu-id="4907a-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="4907a-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4907a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4907a-107">Интерфейс **инапсистемхеалсвалидатионрекуест** предоставляет методы, используемые для поддержки средств проверки работоспособности системы, которые определяются разработчиком приложения.</span><span class="sxs-lookup"><span data-stu-id="4907a-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="4907a-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) наследует все методы этого интерфейса, и вместо него следует использовать.</span><span class="sxs-lookup"><span data-stu-id="4907a-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="4907a-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="4907a-109">Members</span></span>

<span data-ttu-id="4907a-110">Интерфейс **инапсистемхеалсвалидатионрекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4907a-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4907a-111">**Инапсистемхеалсвалидатионрекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4907a-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="4907a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4907a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4907a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4907a-113">Methods</span></span>

<span data-ttu-id="4907a-114">Интерфейс **инапсистемхеалсвалидатионрекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4907a-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="4907a-115">Метод</span><span class="sxs-lookup"><span data-stu-id="4907a-115">Method</span></span>                                                                                                                               | <span data-ttu-id="4907a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4907a-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4907a-117">**Инапсистемхеалсвалидатионрекуест:: Жеткоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="4907a-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="4907a-118">Используется проверяющими элементами управления для получения идентификатора корреляции.</span><span class="sxs-lookup"><span data-stu-id="4907a-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="4907a-119">Затем проверяющий элемент управления должен записать эти сведения в журнал.</span><span class="sxs-lookup"><span data-stu-id="4907a-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="4907a-120">**Инапсистемхеалсвалидатионрекуест:: Жетмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="4907a-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="4907a-121">Используется проверяющими элементами управления для получения имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="4907a-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="4907a-122">Затем проверяющий элемент управления должен записать эти сведения в журнал.</span><span class="sxs-lookup"><span data-stu-id="4907a-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="4907a-123">**Инапсистемхеалсвалидатионрекуест:: Жетприватедата**</span><span class="sxs-lookup"><span data-stu-id="4907a-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="4907a-124">Позволяет Напсервер получать сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="4907a-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="4907a-125">**Инапсистемхеалсвалидатионрекуест:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="4907a-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="4907a-126">Позволяет проверяющим элементам извлекать и проверять сведения Сохрекуест.</span><span class="sxs-lookup"><span data-stu-id="4907a-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="4907a-127">**Инапсистемхеалсвалидатионрекуест:: Жетсохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="4907a-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="4907a-128">Возвращает объект Сохреспонсе.</span><span class="sxs-lookup"><span data-stu-id="4907a-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="4907a-129">**Инапсистемхеалсвалидатионрекуест:: Жетстрингкоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="4907a-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="4907a-130">Используется проверяющими элементами управления для получения уникального идентификатора Exchange.</span><span class="sxs-lookup"><span data-stu-id="4907a-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="4907a-131">Затем проверяющий элемент управления должен записать эти сведения в журнал.</span><span class="sxs-lookup"><span data-stu-id="4907a-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="4907a-132">**Инапсистемхеалсвалидатионрекуест:: Сетприватедата**</span><span class="sxs-lookup"><span data-stu-id="4907a-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="4907a-133">Позволяет Напсервер хранить сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="4907a-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="4907a-134">**Инапсистемхеалсвалидатионрекуест:: Сетсохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="4907a-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="4907a-135">Позволяет средствам проверки задавать Сохреспонсе.</span><span class="sxs-lookup"><span data-stu-id="4907a-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="4907a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="4907a-136">Requirements</span></span>



| <span data-ttu-id="4907a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="4907a-137">Requirement</span></span> | <span data-ttu-id="4907a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="4907a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4907a-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4907a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4907a-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4907a-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="4907a-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4907a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4907a-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4907a-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4907a-143">Header</span><span class="sxs-lookup"><span data-stu-id="4907a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4907a-144"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="4907a-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="4907a-145">IDL</span><span class="sxs-lookup"><span data-stu-id="4907a-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4907a-146"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4907a-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="4907a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4907a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4907a-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4907a-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="4907a-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4907a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4907a-150">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="4907a-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4907a-151">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="4907a-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

