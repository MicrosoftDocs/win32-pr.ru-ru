---
description: Интерфейс Имониторевентер предоставляет методы для отправки событий и выделения и освобождения ресурсов монитора.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Интерфейс Имониторевентер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897178"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="d0ce0-103">Интерфейс Имониторевентер</span><span class="sxs-lookup"><span data-stu-id="d0ce0-103">IMonitorEventer interface</span></span>

<span data-ttu-id="d0ce0-104">Интерфейс **имониторевентер** предоставляет методы для отправки событий и выделения и освобождения ресурсов монитора.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="d0ce0-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="d0ce0-105">Members</span></span>

<span data-ttu-id="d0ce0-106">Интерфейс **имониторевентер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d0ce0-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d0ce0-107">**Имониторевентер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d0ce0-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="d0ce0-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d0ce0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d0ce0-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d0ce0-109">Methods</span></span>

<span data-ttu-id="d0ce0-110">Интерфейс **имониторевентер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="d0ce0-111">Метод</span><span class="sxs-lookup"><span data-stu-id="d0ce0-111">Method</span></span>                                                 | <span data-ttu-id="d0ce0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d0ce0-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="d0ce0-113">**фриевентдата**</span><span class="sxs-lookup"><span data-stu-id="d0ce0-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="d0ce0-114">Освобождает место, выделенное для данных монитора.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="d0ce0-115">**жетевентдата**</span><span class="sxs-lookup"><span data-stu-id="d0ce0-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="d0ce0-116">Выделяет место для данных монитора.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="d0ce0-117">**сенднмевент**</span><span class="sxs-lookup"><span data-stu-id="d0ce0-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="d0ce0-118">Отправляет события в WMI.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d0ce0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d0ce0-119">Requirements</span></span>



| <span data-ttu-id="d0ce0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d0ce0-120">Requirement</span></span> | <span data-ttu-id="d0ce0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d0ce0-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ce0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0ce0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ce0-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0ce0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0ce0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0ce0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ce0-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0ce0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0ce0-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0ce0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ce0-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce0-127"><dt>Netmon.h</dt></span></span> </dl> |



 

