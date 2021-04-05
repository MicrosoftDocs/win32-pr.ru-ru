---
title: Интерфейс Инапкомпонентинфо (Напкоммон. h)
description: Предоставляет методы, которые подключаемые модули (такие как SHA и SHV) должны реализовать, чтобы система защиты доступа к сети могла взаимодействовать с ними.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Инапкомпонентинфо интерфейса NAP
- Инапкомпонентинфо интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988447"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="75424-105">Интерфейс Инапкомпонентинфо</span><span class="sxs-lookup"><span data-stu-id="75424-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="75424-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="75424-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="75424-107">Интерфейс **инапкомпонентинфо** предоставляет методы, которые должны быть реализованы подключаемыми компонентами (например, SHA и SHV), чтобы система NAP могла взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="75424-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="75424-108">Система защиты доступа к сети вызывает реализацию этих методов для получения статических административных данных (например, понятного имени или локализованных строк).</span><span class="sxs-lookup"><span data-stu-id="75424-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="75424-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="75424-109">Members</span></span>

<span data-ttu-id="75424-110">Интерфейс **инапкомпонентинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="75424-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="75424-111">**Инапкомпонентинфо** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="75424-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="75424-112">Методы</span><span class="sxs-lookup"><span data-stu-id="75424-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="75424-113">Методы</span><span class="sxs-lookup"><span data-stu-id="75424-113">Methods</span></span>

<span data-ttu-id="75424-114">Интерфейс **инапкомпонентинфо** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="75424-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="75424-115">Метод</span><span class="sxs-lookup"><span data-stu-id="75424-115">Method</span></span>                                                                                                         | <span data-ttu-id="75424-116">Описание</span><span class="sxs-lookup"><span data-stu-id="75424-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75424-117">**Инапкомпонентинфо:: Конвертерроркодетомессажеид**</span><span class="sxs-lookup"><span data-stu-id="75424-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="75424-118">Используется системой защиты доступа к сети для запроса клиента работоспособности при преобразовании кода ошибки HRESULT в идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="75424-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="75424-119">**Инапкомпонентинфо::, описание**</span><span class="sxs-lookup"><span data-stu-id="75424-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="75424-120">Используется системой защиты доступа к сети для получения описания клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75424-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="75424-121">**Инапкомпонентинфо:: Жетфриендлинаме**</span><span class="sxs-lookup"><span data-stu-id="75424-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="75424-122">Используется системой защиты доступа к сети для получения понятного имени клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75424-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="75424-123">**Инапкомпонентинфо:: "Icon"**</span><span class="sxs-lookup"><span data-stu-id="75424-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="75424-124">Используется системой защиты доступа к сети для получения значка клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75424-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="75424-125">**Инапкомпонентинфо:: Жетлокализедстринг**</span><span class="sxs-lookup"><span data-stu-id="75424-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="75424-126">Используется системой защиты доступа к сети для получения локализованных строк.</span><span class="sxs-lookup"><span data-stu-id="75424-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="75424-127">**Инапкомпонентинфо:: Жетвендорнаме**</span><span class="sxs-lookup"><span data-stu-id="75424-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="75424-128">Используется системой защиты доступа к сети для получения имени поставщика клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75424-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="75424-129">**Инапкомпонентинфо::/версия**</span><span class="sxs-lookup"><span data-stu-id="75424-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="75424-130">Используется системой защиты доступа к сети для получения версии клиента работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75424-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="75424-131">Требования</span><span class="sxs-lookup"><span data-stu-id="75424-131">Requirements</span></span>



| <span data-ttu-id="75424-132">Требование</span><span class="sxs-lookup"><span data-stu-id="75424-132">Requirement</span></span> | <span data-ttu-id="75424-133">Значение</span><span class="sxs-lookup"><span data-stu-id="75424-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75424-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75424-134">Minimum supported client</span></span><br/> | <span data-ttu-id="75424-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75424-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75424-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75424-136">Minimum supported server</span></span><br/> | <span data-ttu-id="75424-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75424-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="75424-138">Header</span><span class="sxs-lookup"><span data-stu-id="75424-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="75424-139"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="75424-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="75424-140">IDL</span><span class="sxs-lookup"><span data-stu-id="75424-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75424-141"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75424-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75424-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75424-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75424-143">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="75424-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="75424-144">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="75424-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

