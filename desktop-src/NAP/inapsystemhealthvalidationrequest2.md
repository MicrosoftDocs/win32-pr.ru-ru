---
title: Интерфейс INapSystemHealthValidationRequest2 (Напсистемхеалсвалидатор. h)
description: Предоставляет методы, используемые для поддержки средств проверки работоспособности системы, которые определяются разработчиком приложения.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 интерфейса NAP
- INapSystemHealthValidationRequest2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672913"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="b9591-105">Интерфейс INapSystemHealthValidationRequest2</span><span class="sxs-lookup"><span data-stu-id="b9591-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="b9591-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b9591-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b9591-107">Интерфейс **INapSystemHealthValidationRequest2** предоставляет методы, используемые для поддержки средств проверки работоспособности системы, которые определяются разработчиком приложения.</span><span class="sxs-lookup"><span data-stu-id="b9591-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="b9591-108">Этот интерфейс наследует все методы [**инапсистемхеалсвалидатионрекуест**](inapsystemhealthvalidationrequest.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="b9591-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="b9591-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="b9591-109">Members</span></span>

<span data-ttu-id="b9591-110">Интерфейс **INapSystemHealthValidationRequest2** наследует от [**инапсистемхеалсвалидатионрекуест**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="b9591-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="b9591-111">**INapSystemHealthValidationRequest2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b9591-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="b9591-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b9591-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9591-113">Методы</span><span class="sxs-lookup"><span data-stu-id="b9591-113">Methods</span></span>

<span data-ttu-id="b9591-114">Интерфейс **INapSystemHealthValidationRequest2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b9591-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="b9591-115">Метод</span><span class="sxs-lookup"><span data-stu-id="b9591-115">Method</span></span>                                                                                                    | <span data-ttu-id="b9591-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b9591-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="b9591-117">**INapSystemHealthValidationRequest2:: Жетконфигид**</span><span class="sxs-lookup"><span data-stu-id="b9591-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="b9591-118">Извлекает идентификатор конфигурации в запросе на проверку.</span><span class="sxs-lookup"><span data-stu-id="b9591-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9591-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9591-119">Remarks</span></span>

<span data-ttu-id="b9591-120">Если SHV не поддерживает [**INapComponentConfig3**](inapcomponentconfig3.md), этот интерфейс не применяется.</span><span class="sxs-lookup"><span data-stu-id="b9591-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9591-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b9591-121">Requirements</span></span>



| <span data-ttu-id="b9591-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b9591-122">Requirement</span></span> | <span data-ttu-id="b9591-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b9591-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9591-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9591-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9591-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b9591-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="b9591-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9591-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9591-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9591-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b9591-128">Header</span><span class="sxs-lookup"><span data-stu-id="b9591-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9591-129"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9591-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9591-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b9591-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9591-131"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9591-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9591-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b9591-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9591-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9591-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="b9591-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9591-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9591-135">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="b9591-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="b9591-136">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="b9591-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b9591-137">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="b9591-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





