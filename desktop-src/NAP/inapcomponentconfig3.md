---
title: Интерфейс INapComponentConfig3 (Напкоммон. h)
description: Предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для установки и изменения данных конфигурации для конкретного идентификатора конфигурации.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 интерфейса NAP
- INapComponentConfig3 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672488"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="bfa50-105">Интерфейс INapComponentConfig3</span><span class="sxs-lookup"><span data-stu-id="bfa50-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="bfa50-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="bfa50-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bfa50-107">Интерфейс **INapComponentConfig3** предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для установки и изменения данных конфигурации для конкретного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfa50-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="bfa50-108">Этот интерфейс наследует все методы [**INapComponentConfig2**](inapcomponentconfig2.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="bfa50-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="bfa50-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="bfa50-109">Members</span></span>

<span data-ttu-id="bfa50-110">Интерфейс **INapComponentConfig3** наследует от [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="bfa50-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="bfa50-111">**INapComponentConfig3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bfa50-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="bfa50-112">Методы</span><span class="sxs-lookup"><span data-stu-id="bfa50-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bfa50-113">Методы</span><span class="sxs-lookup"><span data-stu-id="bfa50-113">Methods</span></span>

<span data-ttu-id="bfa50-114">Интерфейс **INapComponentConfig3** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bfa50-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="bfa50-115">Метод</span><span class="sxs-lookup"><span data-stu-id="bfa50-115">Method</span></span>                                                                                | <span data-ttu-id="bfa50-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bfa50-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfa50-117">**INapComponentConfig3::D Елетеаллконфиг**</span><span class="sxs-lookup"><span data-stu-id="bfa50-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="bfa50-118">Реализуется средствами SHV для предоставления способа сброса хранилища SHV в исходное состояние после установки.</span><span class="sxs-lookup"><span data-stu-id="bfa50-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="bfa50-119">**INapComponentConfig3::D Елетеконфиг**</span><span class="sxs-lookup"><span data-stu-id="bfa50-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="bfa50-120">Реализуется средствами SHV для предоставления способа удаления данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfa50-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="bfa50-121">**INapComponentConfig3:: Жетконфигфромид**</span><span class="sxs-lookup"><span data-stu-id="bfa50-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="bfa50-122">Реализуется средствами SHV, чтобы предоставить способ получения данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfa50-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="bfa50-123">**INapComponentConfig3:: документе newconfig**</span><span class="sxs-lookup"><span data-stu-id="bfa50-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="bfa50-124">Реализуется средствами SHV, чтобы предоставить способ создания данных конфигурации для определенного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfa50-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="bfa50-125">**INapComponentConfig3:: Сетконфигтоид**</span><span class="sxs-lookup"><span data-stu-id="bfa50-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="bfa50-126">Реализуется средствами SHV для предоставления способа установки данных конфигурации для конкретного идентификатора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfa50-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfa50-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfa50-127">Remarks</span></span>

<span data-ttu-id="bfa50-128">Этот интерфейс не должен реализовываться агентами работоспособности системы (SHA) или клиентами принудительного применения карантина (кекс).</span><span class="sxs-lookup"><span data-stu-id="bfa50-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa50-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bfa50-129">Requirements</span></span>



| <span data-ttu-id="bfa50-130">Требование</span><span class="sxs-lookup"><span data-stu-id="bfa50-130">Requirement</span></span> | <span data-ttu-id="bfa50-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa50-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa50-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfa50-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa50-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bfa50-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bfa50-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfa50-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa50-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfa50-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfa50-136">Header</span><span class="sxs-lookup"><span data-stu-id="bfa50-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa50-137"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa50-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfa50-138">IDL</span><span class="sxs-lookup"><span data-stu-id="bfa50-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfa50-139"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfa50-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa50-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfa50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa50-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="bfa50-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="bfa50-142">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="bfa50-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bfa50-143">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="bfa50-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





