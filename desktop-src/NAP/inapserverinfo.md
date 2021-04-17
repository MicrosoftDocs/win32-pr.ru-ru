---
title: Интерфейс Инапсерверинфо (Напсерверманажемент. h)
description: Клиенты управления (например, поставщики WMI или программы командной строки) используют для запроса состояния системы сервера защиты доступа к сети.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Инапсерверинфо интерфейса NAP
- Инапсерверинфо интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672698"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="99b9a-105">Интерфейс Инапсерверинфо</span><span class="sxs-lookup"><span data-stu-id="99b9a-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="99b9a-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="99b9a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="99b9a-107">**Инапсерверинфо** предоставляет методы, которые клиенты управления (например, поставщики WMI или программы командной строки) используют для запроса состояния системы сервера защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="99b9a-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="99b9a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="99b9a-108">Members</span></span>

<span data-ttu-id="99b9a-109">Интерфейс **инапсерверинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="99b9a-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="99b9a-110">**Инапсерверинфо** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="99b9a-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="99b9a-111">Методы</span><span class="sxs-lookup"><span data-stu-id="99b9a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="99b9a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="99b9a-112">Methods</span></span>

<span data-ttu-id="99b9a-113">Интерфейс **инапсерверинфо** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="99b9a-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="99b9a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="99b9a-114">Method</span></span>                                                                                                                   | <span data-ttu-id="99b9a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="99b9a-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="99b9a-116">**Инапсерверинфо:: Жетфаилурекатегоримаппингс**</span><span class="sxs-lookup"><span data-stu-id="99b9a-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="99b9a-117">Извлекает сопоставления категорий сбоев для указанного SHV.</span><span class="sxs-lookup"><span data-stu-id="99b9a-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="99b9a-118">**Инапсерверинфо:: Жетнапсерверинфо**</span><span class="sxs-lookup"><span data-stu-id="99b9a-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="99b9a-119">Извлекает сведения о сервере NAP.</span><span class="sxs-lookup"><span data-stu-id="99b9a-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="99b9a-120">**Инапсерверинфо:: Жетрегистередсистемхеалсвалидаторс**</span><span class="sxs-lookup"><span data-stu-id="99b9a-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="99b9a-121">Извлекает список зарегистрированных SHV.</span><span class="sxs-lookup"><span data-stu-id="99b9a-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="99b9a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99b9a-122">Remarks</span></span>

<span data-ttu-id="99b9a-123">Эти методы предоставляют только статические сведения о сервере NAP и его компонентах в системе.</span><span class="sxs-lookup"><span data-stu-id="99b9a-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b9a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="99b9a-124">Requirements</span></span>



| <span data-ttu-id="99b9a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="99b9a-125">Requirement</span></span> | <span data-ttu-id="99b9a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="99b9a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b9a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99b9a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99b9a-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="99b9a-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="99b9a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99b9a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99b9a-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99b9a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99b9a-131">Header</span><span class="sxs-lookup"><span data-stu-id="99b9a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b9a-132"><dt>Напсерверманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b9a-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="99b9a-133">IDL</span><span class="sxs-lookup"><span data-stu-id="99b9a-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99b9a-134"><dt>Напсерверманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99b9a-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="99b9a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="99b9a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b9a-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b9a-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="99b9a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99b9a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b9a-138">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="99b9a-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="99b9a-139">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="99b9a-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

