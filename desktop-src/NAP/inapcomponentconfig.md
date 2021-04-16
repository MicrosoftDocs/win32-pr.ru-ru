---
title: Интерфейс Инапкомпонентконфиг (Напкоммон. h)
description: Предоставляет методы конфигурации системы защиты доступа к сети для средств проверки работоспособности системы (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Инапкомпонентконфиг интерфейса NAP
- Инапкомпонентконфиг интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415265"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="93b72-105">Интерфейс Инапкомпонентконфиг</span><span class="sxs-lookup"><span data-stu-id="93b72-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="93b72-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="93b72-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="93b72-107">Интерфейс **инапкомпонентконфиг** предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV).</span><span class="sxs-lookup"><span data-stu-id="93b72-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="93b72-108">[**INapComponentConfig2**](inapcomponentconfig2.md) и [**INapComponentConfig3**](inapcomponentconfig3.md) наследуют все методы этого интерфейса и должны использоваться вместо них.</span><span class="sxs-lookup"><span data-stu-id="93b72-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="93b72-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="93b72-109">Members</span></span>

<span data-ttu-id="93b72-110">Интерфейс **инапкомпонентконфиг** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="93b72-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93b72-111">**Инапкомпонентконфиг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93b72-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="93b72-112">Методы</span><span class="sxs-lookup"><span data-stu-id="93b72-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93b72-113">Методы</span><span class="sxs-lookup"><span data-stu-id="93b72-113">Methods</span></span>

<span data-ttu-id="93b72-114">Интерфейс **инапкомпонентконфиг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="93b72-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="93b72-115">Метод</span><span class="sxs-lookup"><span data-stu-id="93b72-115">Method</span></span>                                                                          | <span data-ttu-id="93b72-116">Описание</span><span class="sxs-lookup"><span data-stu-id="93b72-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="93b72-117">**Инапкомпонентконфиг:: config**</span><span class="sxs-lookup"><span data-stu-id="93b72-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="93b72-118">Извлекает конфигурацию компонента SHV.</span><span class="sxs-lookup"><span data-stu-id="93b72-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="93b72-119">**Инапкомпонентконфиг:: Инвокеуи**</span><span class="sxs-lookup"><span data-stu-id="93b72-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="93b72-120">Запускает настраиваемый пользовательский интерфейс для компонента SHV.</span><span class="sxs-lookup"><span data-stu-id="93b72-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="93b72-121">**Инапкомпонентконфиг:: Исуисуппортед**</span><span class="sxs-lookup"><span data-stu-id="93b72-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="93b72-122">Указывает, поддерживает ли компонент SHV настроенный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="93b72-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="93b72-123">**Инапкомпонентконфиг:: Сетконфиг**</span><span class="sxs-lookup"><span data-stu-id="93b72-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="93b72-124">Задает конфигурацию компонента SHV.</span><span class="sxs-lookup"><span data-stu-id="93b72-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="93b72-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93b72-125">Remarks</span></span>

<span data-ttu-id="93b72-126">Этот интерфейс не должен реализовываться агентами работоспособности системы (SHA) или клиентами принудительного применения карантина (кекс).</span><span class="sxs-lookup"><span data-stu-id="93b72-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="93b72-127">Требования</span><span class="sxs-lookup"><span data-stu-id="93b72-127">Requirements</span></span>



| <span data-ttu-id="93b72-128">Требование</span><span class="sxs-lookup"><span data-stu-id="93b72-128">Requirement</span></span> | <span data-ttu-id="93b72-129">Значение</span><span class="sxs-lookup"><span data-stu-id="93b72-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b72-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93b72-130">Minimum supported client</span></span><br/> | <span data-ttu-id="93b72-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93b72-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="93b72-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93b72-132">Minimum supported server</span></span><br/> | <span data-ttu-id="93b72-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93b72-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="93b72-134">Header</span><span class="sxs-lookup"><span data-stu-id="93b72-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="93b72-135"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="93b72-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="93b72-136">IDL</span><span class="sxs-lookup"><span data-stu-id="93b72-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93b72-137"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93b72-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b72-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93b72-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b72-139">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="93b72-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="93b72-140">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="93b72-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

