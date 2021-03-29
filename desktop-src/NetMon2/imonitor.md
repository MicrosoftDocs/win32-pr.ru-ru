---
description: Интерфейс Имонитор предоставляет методы, управляющие операциями мониторинга. Эти методы вызываются службой контроля мониторинга (МКСВК).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Интерфейс Имонитор (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898038"
---
# <a name="imonitor-interface"></a><span data-ttu-id="70c06-104">Интерфейс Имонитор</span><span class="sxs-lookup"><span data-stu-id="70c06-104">IMonitor interface</span></span>

<span data-ttu-id="70c06-105">Интерфейс **имонитор** предоставляет методы, управляющие операциями мониторинга.</span><span class="sxs-lookup"><span data-stu-id="70c06-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="70c06-106">Эти методы вызываются [*службой контроля мониторинга*](m.md) (мксвк).</span><span class="sxs-lookup"><span data-stu-id="70c06-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="70c06-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="70c06-107">Members</span></span>

<span data-ttu-id="70c06-108">Интерфейс **имонитор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="70c06-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="70c06-109">**Имонитор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70c06-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="70c06-110">Методы</span><span class="sxs-lookup"><span data-stu-id="70c06-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70c06-111">Методы</span><span class="sxs-lookup"><span data-stu-id="70c06-111">Methods</span></span>

<span data-ttu-id="70c06-112">Интерфейс **имонитор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="70c06-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="70c06-113">Метод</span><span class="sxs-lookup"><span data-stu-id="70c06-113">Method</span></span>                                        | <span data-ttu-id="70c06-114">Описание</span><span class="sxs-lookup"><span data-stu-id="70c06-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70c06-115">**доконфигуре**</span><span class="sxs-lookup"><span data-stu-id="70c06-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="70c06-116">Обновляет конфигурацию монитора.</span><span class="sxs-lookup"><span data-stu-id="70c06-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="70c06-117">**доинитиализе**</span><span class="sxs-lookup"><span data-stu-id="70c06-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="70c06-118">Инициализирует монитор.</span><span class="sxs-lookup"><span data-stu-id="70c06-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="70c06-119">**Выкадровки**</span><span class="sxs-lookup"><span data-stu-id="70c06-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="70c06-120">Указывает состояние события кадра.</span><span class="sxs-lookup"><span data-stu-id="70c06-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="70c06-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="70c06-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="70c06-122">Указывает, что монитор успешно настроен и начинается сбор данных.</span><span class="sxs-lookup"><span data-stu-id="70c06-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="70c06-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="70c06-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="70c06-124">Указывает на событие состояния НПП.</span><span class="sxs-lookup"><span data-stu-id="70c06-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="70c06-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="70c06-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="70c06-126">Указывает на завершение отслеживания данных.</span><span class="sxs-lookup"><span data-stu-id="70c06-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="70c06-127">Требования</span><span class="sxs-lookup"><span data-stu-id="70c06-127">Requirements</span></span>



| <span data-ttu-id="70c06-128">Требование</span><span class="sxs-lookup"><span data-stu-id="70c06-128">Requirement</span></span> | <span data-ttu-id="70c06-129">Значение</span><span class="sxs-lookup"><span data-stu-id="70c06-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70c06-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c06-130">Minimum supported client</span></span><br/> | <span data-ttu-id="70c06-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70c06-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="70c06-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c06-132">Minimum supported server</span></span><br/> | <span data-ttu-id="70c06-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70c06-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="70c06-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="70c06-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c06-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c06-135"><dt>Netmon.h</dt></span></span> </dl> |



 

