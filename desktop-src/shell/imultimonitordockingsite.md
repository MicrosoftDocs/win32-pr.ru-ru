---
description: Реализуется браузером. Предоставляет методы, управляющие монитором, содержащим панель задач Windows в системе с несколькими мониторами.
title: Интерфейс Имултимонитордоккингсите
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997966"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="20409-104">Интерфейс Имултимонитордоккингсите</span><span class="sxs-lookup"><span data-stu-id="20409-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="20409-105">Реализуется браузером.</span><span class="sxs-lookup"><span data-stu-id="20409-105">Implemented by the browser.</span></span> <span data-ttu-id="20409-106">Предоставляет методы, управляющие монитором, содержащим панель задач Windows в системе с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="20409-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="20409-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="20409-107">Members</span></span>

<span data-ttu-id="20409-108">Интерфейс **имултимонитордоккингсите** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="20409-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="20409-109">**Имултимонитордоккингсите** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20409-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="20409-110">Методы</span><span class="sxs-lookup"><span data-stu-id="20409-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20409-111">Методы</span><span class="sxs-lookup"><span data-stu-id="20409-111">Methods</span></span>

<span data-ttu-id="20409-112">Интерфейс **имултимонитордоккингсите** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="20409-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="20409-113">Метод</span><span class="sxs-lookup"><span data-stu-id="20409-113">Method</span></span>                                                            | <span data-ttu-id="20409-114">Описание</span><span class="sxs-lookup"><span data-stu-id="20409-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20409-115">**Монитор**</span><span class="sxs-lookup"><span data-stu-id="20409-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="20409-116">Возвращает текущий монитор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20409-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="20409-117">**рекуестмонитор**</span><span class="sxs-lookup"><span data-stu-id="20409-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="20409-118">Проверяет, что монитор активен и доступен.</span><span class="sxs-lookup"><span data-stu-id="20409-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="20409-119">**сетмонитор**</span><span class="sxs-lookup"><span data-stu-id="20409-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="20409-120">Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="20409-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20409-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="20409-121">Remarks</span></span>

<span data-ttu-id="20409-122">Обычно интерфейс **имултимонитордоккингсите** не реализуется.</span><span class="sxs-lookup"><span data-stu-id="20409-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="20409-123">Браузер оболочки реализует этот интерфейс для поддержки нескольких мониторов.</span><span class="sxs-lookup"><span data-stu-id="20409-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="20409-124">Требования</span><span class="sxs-lookup"><span data-stu-id="20409-124">Requirements</span></span>



| <span data-ttu-id="20409-125">Требование</span><span class="sxs-lookup"><span data-stu-id="20409-125">Requirement</span></span> | <span data-ttu-id="20409-126">Значение</span><span class="sxs-lookup"><span data-stu-id="20409-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="20409-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20409-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20409-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="20409-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="20409-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20409-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20409-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20409-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
