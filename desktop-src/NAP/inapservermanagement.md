---
title: Интерфейс Инапсерверманажемент (Напсерверманажемент. h)
description: Используются для управления сервером защиты доступа к сети.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- Инапсерверманажемент интерфейса NAP
- Инапсерверманажемент интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136210"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="dff98-105">Интерфейс Инапсерверманажемент</span><span class="sxs-lookup"><span data-stu-id="dff98-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="dff98-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="dff98-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dff98-107">**Инапсерверманажемент** предоставляет методы, используемые для управления сервером NAP.</span><span class="sxs-lookup"><span data-stu-id="dff98-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="dff98-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="dff98-108">Members</span></span>

<span data-ttu-id="dff98-109">Интерфейс **инапсерверманажемент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dff98-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dff98-110">**Инапсерверманажемент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dff98-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="dff98-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dff98-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dff98-112">Методы</span><span class="sxs-lookup"><span data-stu-id="dff98-112">Methods</span></span>

<span data-ttu-id="dff98-113">Интерфейс **инапсерверманажемент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dff98-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="dff98-114">Метод</span><span class="sxs-lookup"><span data-stu-id="dff98-114">Method</span></span>                                                                                                                       | <span data-ttu-id="dff98-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dff98-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="dff98-116">**Инапсерверманажемент:: Регистерсистемхеалсвалидатор**</span><span class="sxs-lookup"><span data-stu-id="dff98-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="dff98-117">Регистрирует SHV.</span><span class="sxs-lookup"><span data-stu-id="dff98-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="dff98-118">**Инапсерверманажемент:: Сетфаилурекатегоримаппингс**</span><span class="sxs-lookup"><span data-stu-id="dff98-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="dff98-119">Задает сопоставления категорий сбоев SHV.</span><span class="sxs-lookup"><span data-stu-id="dff98-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="dff98-120">**Инапсерверманажемент:: Унрегистерсистемхеалсвалидатор**</span><span class="sxs-lookup"><span data-stu-id="dff98-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="dff98-121">Отменяет регистрацию SHV на сервере NAP.</span><span class="sxs-lookup"><span data-stu-id="dff98-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="dff98-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dff98-122">Requirements</span></span>



| <span data-ttu-id="dff98-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dff98-123">Requirement</span></span> | <span data-ttu-id="dff98-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dff98-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dff98-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dff98-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dff98-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dff98-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="dff98-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dff98-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dff98-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dff98-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dff98-129">Header</span><span class="sxs-lookup"><span data-stu-id="dff98-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff98-130"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff98-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="dff98-131">IDL</span><span class="sxs-lookup"><span data-stu-id="dff98-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dff98-132"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dff98-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="dff98-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dff98-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dff98-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dff98-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="dff98-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff98-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff98-136">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="dff98-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="dff98-137">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="dff98-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

