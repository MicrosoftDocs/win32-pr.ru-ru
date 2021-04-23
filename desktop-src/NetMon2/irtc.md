---
description: Интерфейс ИРТК предоставляет методы, используемые для подключения НПП к сети, записи сетевого трафика, получения статистики и отключения НПП от сети.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Интерфейс ИРТК (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991571"
---
# <a name="irtc-interface"></a><span data-ttu-id="dc42b-103">Интерфейс ИРТК</span><span class="sxs-lookup"><span data-stu-id="dc42b-103">IRTC interface</span></span>

<span data-ttu-id="dc42b-104">Интерфейс **ИРТК** предоставляет методы, используемые для подключения НПП к сети, записи сетевого трафика, получения статистики и отключения НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="dc42b-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="dc42b-105">**ИРТК** получает интерфейс для локальных точек входа, которые необходимы для участия в записи в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="dc42b-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="dc42b-106">Этот интерфейс включает метод, который передает обратный вызов НПП.</span><span class="sxs-lookup"><span data-stu-id="dc42b-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="dc42b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc42b-107">Members</span></span>

<span data-ttu-id="dc42b-108">Интерфейс **ИРТК** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc42b-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc42b-109">**ИРТК** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc42b-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="dc42b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="dc42b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc42b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dc42b-111">Methods</span></span>

<span data-ttu-id="dc42b-112">Интерфейс **ИРТК** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc42b-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="dc42b-113">Метод</span><span class="sxs-lookup"><span data-stu-id="dc42b-113">Method</span></span>                                                              | <span data-ttu-id="dc42b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dc42b-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc42b-115">**Configure**</span><span class="sxs-lookup"><span data-stu-id="dc42b-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="dc42b-116">Задает триггер, соответствие шаблону и размер буфера записи.</span><span class="sxs-lookup"><span data-stu-id="dc42b-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="dc42b-117">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="dc42b-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="dc42b-118">Подключает НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="dc42b-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="dc42b-119">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="dc42b-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="dc42b-120">Отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="dc42b-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dc42b-121">**жетконтролстате**</span><span class="sxs-lookup"><span data-stu-id="dc42b-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="dc42b-122">Возвращает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="dc42b-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="dc42b-123">**жетконверсатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="dc42b-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="dc42b-124">Извлекает [*сведения о*](s.md) [*сеансе*](s.md) и станции для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="dc42b-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="dc42b-125">**жеттоталстатистикс**</span><span class="sxs-lookup"><span data-stu-id="dc42b-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="dc42b-126">Извлекает сведения о времени, буфере, драйвере и другой сетевой статистике из выполняемой в данный момент записи.</span><span class="sxs-lookup"><span data-stu-id="dc42b-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="dc42b-127">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="dc42b-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="dc42b-128">Временно останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="dc42b-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="dc42b-129">**куеристатионс**</span><span class="sxs-lookup"><span data-stu-id="dc42b-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="dc42b-130">Извлекает список всех компьютеров в подсети, которые используют сетевой монитор для записи сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="dc42b-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="dc42b-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="dc42b-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="dc42b-132">Получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="dc42b-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="dc42b-133">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="dc42b-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="dc42b-134">Перезапускает приостановленную запись.</span><span class="sxs-lookup"><span data-stu-id="dc42b-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="dc42b-135">**Начать**</span><span class="sxs-lookup"><span data-stu-id="dc42b-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="dc42b-136">Запускает запись.</span><span class="sxs-lookup"><span data-stu-id="dc42b-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="dc42b-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="dc42b-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="dc42b-138">Останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="dc42b-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="dc42b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="dc42b-139">Requirements</span></span>



| <span data-ttu-id="dc42b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="dc42b-140">Requirement</span></span> | <span data-ttu-id="dc42b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="dc42b-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc42b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc42b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dc42b-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc42b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dc42b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc42b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dc42b-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc42b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dc42b-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dc42b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc42b-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc42b-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dc42b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="dc42b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc42b-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc42b-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

