---
title: Интерфейс INapClientManagement2 (Напманажемент. h)
description: Предоставляет методы для управления клиентами NAP. | Интерфейс INapClientManagement2 (Напманажемент. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 интерфейса NAP
- INapClientManagement2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081816"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="59de1-106">Интерфейс INapClientManagement2</span><span class="sxs-lookup"><span data-stu-id="59de1-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="59de1-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="59de1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="59de1-108">Интерфейс **INapClientManagement2** предоставляет методы для управления клиентами NAP.</span><span class="sxs-lookup"><span data-stu-id="59de1-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="59de1-109">Этот интерфейс наследует все методы [**инапклиентманажемент**](inapclientmanagement.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="59de1-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="59de1-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="59de1-110">Members</span></span>

<span data-ttu-id="59de1-111">Интерфейс **INapClientManagement2** наследует от [**инапклиентманажемент**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="59de1-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="59de1-112">**INapClientManagement2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="59de1-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="59de1-113">Методы</span><span class="sxs-lookup"><span data-stu-id="59de1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59de1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="59de1-114">Methods</span></span>

<span data-ttu-id="59de1-115">Интерфейс **INapClientManagement2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="59de1-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="59de1-116">Метод</span><span class="sxs-lookup"><span data-stu-id="59de1-116">Method</span></span>                                                                                                    | <span data-ttu-id="59de1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="59de1-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59de1-118">**INapClientManagement2:: Жетсистемисолатионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="59de1-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="59de1-119">Извлекает сведения о состоянии изоляции и расширенном состоянии изоляции клиента NAP.</span><span class="sxs-lookup"><span data-stu-id="59de1-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59de1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="59de1-120">Requirements</span></span>



| <span data-ttu-id="59de1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="59de1-121">Requirement</span></span> | <span data-ttu-id="59de1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="59de1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59de1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59de1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59de1-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59de1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="59de1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59de1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59de1-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59de1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="59de1-127">Header</span><span class="sxs-lookup"><span data-stu-id="59de1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59de1-128"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="59de1-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="59de1-129">IDL</span><span class="sxs-lookup"><span data-stu-id="59de1-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59de1-130"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59de1-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="59de1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="59de1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59de1-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59de1-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="59de1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59de1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59de1-134">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="59de1-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="59de1-135">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="59de1-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="59de1-136">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="59de1-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





