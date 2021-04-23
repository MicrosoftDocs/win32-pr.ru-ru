---
description: Интерфейс ИЕСП предоставляет методы для подключения НПП к сети, записи сетевого трафика в файл записи, получения статистики и отключения НПП от сети.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Интерфейс ИЕСП (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144653"
---
# <a name="iesp-interface"></a><span data-ttu-id="a2366-103">Интерфейс ИЕСП</span><span class="sxs-lookup"><span data-stu-id="a2366-103">IESP interface</span></span>

<span data-ttu-id="a2366-104">Интерфейс **ИЕСП** предоставляет методы для подключения НПП к сети, записи сетевого трафика в файл записи, получения статистики и отключения НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="a2366-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="a2366-105">Этот интерфейс используется в основном при необходимости сбора [*статистики сетевого диалога*](c.md) в собственном формате файла ESP.</span><span class="sxs-lookup"><span data-stu-id="a2366-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="a2366-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="a2366-106">Members</span></span>

<span data-ttu-id="a2366-107">Интерфейс **ИЕСП** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a2366-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a2366-108">**ИЕСП** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2366-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="a2366-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a2366-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a2366-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a2366-110">Methods</span></span>

<span data-ttu-id="a2366-111">Интерфейс **ИЕСП** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a2366-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="a2366-112">Метод</span><span class="sxs-lookup"><span data-stu-id="a2366-112">Method</span></span>                                          | <span data-ttu-id="a2366-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a2366-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2366-114">**Configure**</span><span class="sxs-lookup"><span data-stu-id="a2366-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="a2366-115">Отправка сведений о конфигурации для записи</span><span class="sxs-lookup"><span data-stu-id="a2366-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="a2366-116">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="a2366-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="a2366-117">Подключает НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="a2366-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="a2366-118">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="a2366-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="a2366-119">Отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="a2366-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a2366-120">**жетконтролстате**</span><span class="sxs-lookup"><span data-stu-id="a2366-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="a2366-121">Возвращает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="a2366-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="a2366-122">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="a2366-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="a2366-123">Временно останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="a2366-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="a2366-124">**куеристатионс**</span><span class="sxs-lookup"><span data-stu-id="a2366-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="a2366-125">Извлекает список всех компьютеров, использующих сетевой монитор для сбора данных в подсети.</span><span class="sxs-lookup"><span data-stu-id="a2366-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="a2366-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="a2366-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="a2366-127">Получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="a2366-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="a2366-128">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="a2366-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="a2366-129">Возобновляет приостановленную запись.</span><span class="sxs-lookup"><span data-stu-id="a2366-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="a2366-130">**Начать**</span><span class="sxs-lookup"><span data-stu-id="a2366-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="a2366-131">Запускает запись и создает файл записи.</span><span class="sxs-lookup"><span data-stu-id="a2366-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="a2366-132">**Stop**</span><span class="sxs-lookup"><span data-stu-id="a2366-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="a2366-133">Останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="a2366-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="a2366-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a2366-134">Requirements</span></span>



| <span data-ttu-id="a2366-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a2366-135">Requirement</span></span> | <span data-ttu-id="a2366-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a2366-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2366-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2366-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2366-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2366-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a2366-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2366-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2366-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2366-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a2366-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2366-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2366-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2366-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a2366-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a2366-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2366-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2366-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

