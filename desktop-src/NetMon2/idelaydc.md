---
description: Интерфейс Иделайдк предоставляет методы, используемые для подключения к сети, записи сетевого трафика в файл записи, получения статистики и отключения от сети.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Интерфейс Иделайдк (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682992"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="c1545-103">Интерфейс Иделайдк</span><span class="sxs-lookup"><span data-stu-id="c1545-103">IDelaydC interface</span></span>

<span data-ttu-id="c1545-104">Интерфейс **иделайдк** предоставляет методы, используемые для подключения к сети, записи сетевого трафика в файл записи, получения статистики и отключения от сети.</span><span class="sxs-lookup"><span data-stu-id="c1545-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="c1545-105">Этот интерфейс захватывает кадры из потока сетевых данных, а затем копирует кадры в файл записи.</span><span class="sxs-lookup"><span data-stu-id="c1545-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="c1545-106">Этот интерфейс используется приложениями сетевой монитор и НПП.</span><span class="sxs-lookup"><span data-stu-id="c1545-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="c1545-107">Для получения сетевых данных целевой сетевой адаптер должен поддерживать неизбирательный режим.</span><span class="sxs-lookup"><span data-stu-id="c1545-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="c1545-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c1545-108">Members</span></span>

<span data-ttu-id="c1545-109">Интерфейс **иделайдк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c1545-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c1545-110">**Иделайдк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1545-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="c1545-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c1545-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1545-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c1545-112">Methods</span></span>

<span data-ttu-id="c1545-113">Интерфейс **иделайдк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c1545-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="c1545-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c1545-114">Method</span></span>                                                                  | <span data-ttu-id="c1545-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c1545-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1545-116">**Configure**</span><span class="sxs-lookup"><span data-stu-id="c1545-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="c1545-117">Отправляет сведения о конфигурации, используемые для записи.</span><span class="sxs-lookup"><span data-stu-id="c1545-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c1545-118">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="c1545-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="c1545-119">Подключает НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="c1545-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c1545-120">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="c1545-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="c1545-121">Отключает НПП от сети.</span><span class="sxs-lookup"><span data-stu-id="c1545-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c1545-122">**жетконтролстате**</span><span class="sxs-lookup"><span data-stu-id="c1545-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="c1545-123">Возвращает состояние [*записи*](c.md), которое указывает, запущена или приостановлена запись.</span><span class="sxs-lookup"><span data-stu-id="c1545-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="c1545-124">**жетконверсатионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="c1545-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="c1545-125">Извлекает [*сведения о*](s.md) [*сеансе*](s.md) и станции для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c1545-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="c1545-126">**жеттоталстатистикс**</span><span class="sxs-lookup"><span data-stu-id="c1545-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="c1545-127">Извлекает сведения о времени, буфере, драйвере и другой сетевой статистике из выполняемой в данный момент записи.</span><span class="sxs-lookup"><span data-stu-id="c1545-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="c1545-128">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="c1545-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="c1545-129">Временно останавливает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="c1545-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c1545-130">**куеристатионс**</span><span class="sxs-lookup"><span data-stu-id="c1545-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="c1545-131">Извлекает список всех компьютеров, которые используют сетевой монитор для записи данных в подсети.</span><span class="sxs-lookup"><span data-stu-id="c1545-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="c1545-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="c1545-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="c1545-133">Получает состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="c1545-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c1545-134">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="c1545-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="c1545-135">Возобновляет приостановленную запись.</span><span class="sxs-lookup"><span data-stu-id="c1545-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="c1545-136">**Начать**</span><span class="sxs-lookup"><span data-stu-id="c1545-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="c1545-137">Запускает запись и создает [*файл записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="c1545-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="c1545-138">**Stop**</span><span class="sxs-lookup"><span data-stu-id="c1545-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="c1545-139">Останавливает текущую запись и закрывает [*файл записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="c1545-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="c1545-140">Требования</span><span class="sxs-lookup"><span data-stu-id="c1545-140">Requirements</span></span>



| <span data-ttu-id="c1545-141">Требование</span><span class="sxs-lookup"><span data-stu-id="c1545-141">Requirement</span></span> | <span data-ttu-id="c1545-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c1545-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1545-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1545-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c1545-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1545-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c1545-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1545-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c1545-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1545-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c1545-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1545-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1545-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1545-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c1545-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c1545-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1545-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1545-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

