---
description: Интерфейс Истатс предоставляет методы, используемые для подключения НПП к сети, записи сетевого трафика, получения статистики и отключения НПП от сети. Этот интерфейс создает статистику без фреймов.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Интерфейс Истатс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682906"
---
# <a name="istats-interface"></a><span data-ttu-id="7c272-104">Интерфейс Истатс</span><span class="sxs-lookup"><span data-stu-id="7c272-104">IStats interface</span></span>

<span data-ttu-id="7c272-105">Интерфейс **истатс** предоставляет методы, используемые для подключения НПП к сети, записи сетевого трафика, получения статистики и отключения НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="7c272-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="7c272-106">Этот интерфейс создает статистику без фреймов.</span><span class="sxs-lookup"><span data-stu-id="7c272-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="7c272-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="7c272-107">Members</span></span>

<span data-ttu-id="7c272-108">Интерфейс **истатс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7c272-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c272-109">**Истатс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7c272-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="7c272-110">Методы</span><span class="sxs-lookup"><span data-stu-id="7c272-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c272-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7c272-111">Methods</span></span>

<span data-ttu-id="7c272-112">Интерфейс **истатс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7c272-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="7c272-113">Метод</span><span class="sxs-lookup"><span data-stu-id="7c272-113">Method</span></span>                                                                | <span data-ttu-id="7c272-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7c272-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c272-115">**Configure**</span><span class="sxs-lookup"><span data-stu-id="7c272-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="7c272-116">Настраивает триггер, соответствие шаблону и размер буфера для файла записи.</span><span class="sxs-lookup"><span data-stu-id="7c272-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="7c272-117">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="7c272-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="7c272-118">Подключает НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="7c272-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="7c272-119">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="7c272-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="7c272-120">Отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="7c272-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="7c272-121">**жетконтролстате**</span><span class="sxs-lookup"><span data-stu-id="7c272-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="7c272-122">Возвращает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="7c272-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="7c272-123">**жетконверсатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="7c272-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="7c272-124">Извлекает [*сведения о*](s.md) [*сеансе*](s.md) и станции о текущем захвате.</span><span class="sxs-lookup"><span data-stu-id="7c272-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="7c272-125">**жеттоталстатистикс**</span><span class="sxs-lookup"><span data-stu-id="7c272-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="7c272-126">Извлекает сведения о времени, буфере, драйвере и другой сетевой статистике из выполняемой в данный момент записи.</span><span class="sxs-lookup"><span data-stu-id="7c272-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="7c272-127">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="7c272-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="7c272-128">Временно останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="7c272-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="7c272-129">**куеристатионс**</span><span class="sxs-lookup"><span data-stu-id="7c272-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="7c272-130">Извлекает список всех компьютеров, использующих сетевой монитор для сбора данных в подсети.</span><span class="sxs-lookup"><span data-stu-id="7c272-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="7c272-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="7c272-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="7c272-132">Получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="7c272-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="7c272-133">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="7c272-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="7c272-134">Перезапускает приостановленную запись.</span><span class="sxs-lookup"><span data-stu-id="7c272-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="7c272-135">**Начать**</span><span class="sxs-lookup"><span data-stu-id="7c272-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="7c272-136">Запускает запись.</span><span class="sxs-lookup"><span data-stu-id="7c272-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="7c272-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="7c272-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="7c272-138">Останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="7c272-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="7c272-139">Требования</span><span class="sxs-lookup"><span data-stu-id="7c272-139">Requirements</span></span>



| <span data-ttu-id="7c272-140">Требование</span><span class="sxs-lookup"><span data-stu-id="7c272-140">Requirement</span></span> | <span data-ttu-id="7c272-141">Значение</span><span class="sxs-lookup"><span data-stu-id="7c272-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c272-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c272-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7c272-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c272-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7c272-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c272-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7c272-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c272-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7c272-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7c272-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c272-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c272-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7c272-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7c272-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c272-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c272-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

