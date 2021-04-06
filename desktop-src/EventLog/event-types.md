---
description: Существует пять типов событий, которые можно регистрировать. Все они имеют четко определенные общие данные и при необходимости могут включать данные, относящиеся к конкретному событию.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Типы событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908863"
---
# <a name="event-types"></a><span data-ttu-id="d10ef-104">Типы событий</span><span class="sxs-lookup"><span data-stu-id="d10ef-104">Event Types</span></span>

<span data-ttu-id="d10ef-105">Существует пять типов событий, которые можно регистрировать.</span><span class="sxs-lookup"><span data-stu-id="d10ef-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="d10ef-106">Все они имеют четко определенные общие данные и при необходимости могут включать данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="d10ef-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="d10ef-107">Приложение указывает тип события, когда сообщает о событии.</span><span class="sxs-lookup"><span data-stu-id="d10ef-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="d10ef-108">Каждое событие должно принадлежать одному типу.</span><span class="sxs-lookup"><span data-stu-id="d10ef-108">Each event must be of a single type.</span></span> <span data-ttu-id="d10ef-109">Просмотр событий отображает разные значки для каждого типа в представлении списка журнала событий.</span><span class="sxs-lookup"><span data-stu-id="d10ef-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="d10ef-110">В следующей таблице описаны пять типов событий, используемых при ведении журнала событий.</span><span class="sxs-lookup"><span data-stu-id="d10ef-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="d10ef-111">Тип события</span><span class="sxs-lookup"><span data-stu-id="d10ef-111">Event type</span></span>        | <span data-ttu-id="d10ef-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d10ef-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10ef-113">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="d10ef-113">**Error**</span></span>         | <span data-ttu-id="d10ef-114">Событие, указывающее на значительную проблему, например потери данных или потери функциональности.</span><span class="sxs-lookup"><span data-stu-id="d10ef-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="d10ef-115">Например, если при запуске службы не удается загрузить службу, регистрируется событие ошибки.</span><span class="sxs-lookup"><span data-stu-id="d10ef-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="d10ef-116">**Предупреждение**</span><span class="sxs-lookup"><span data-stu-id="d10ef-116">**Warning**</span></span>       | <span data-ttu-id="d10ef-117">Событие, которое не обязательно является существенным, но может указывать на возможную будущую проблему.</span><span class="sxs-lookup"><span data-stu-id="d10ef-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="d10ef-118">Например, если место на диске мало, регистрируется событие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d10ef-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="d10ef-119">Если приложение может восстановиться из события без потери функциональности или данных, оно может классифицировать событие как событие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="d10ef-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="d10ef-120">**Информация**</span><span class="sxs-lookup"><span data-stu-id="d10ef-120">**Information**</span></span>   | <span data-ttu-id="d10ef-121">Событие, описывающее успешную работу приложения, драйвера или службы.</span><span class="sxs-lookup"><span data-stu-id="d10ef-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="d10ef-122">Например, если сетевой драйвер успешно загружается, может быть целесообразно зарегистрировать информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d10ef-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="d10ef-123">Обратите внимание, что как правило, для настольных приложений не требуется регистрировать событие при каждом запуске.</span><span class="sxs-lookup"><span data-stu-id="d10ef-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="d10ef-124">**Аудит успехов**</span><span class="sxs-lookup"><span data-stu-id="d10ef-124">**Success Audit**</span></span> | <span data-ttu-id="d10ef-125">Событие, которое регистрирует успешную попытку безопасного доступа.</span><span class="sxs-lookup"><span data-stu-id="d10ef-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="d10ef-126">Например, успешная попытка входа пользователя в систему регистрируется как событие успешного аудита.</span><span class="sxs-lookup"><span data-stu-id="d10ef-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="d10ef-127">**Аудит ошибок**</span><span class="sxs-lookup"><span data-stu-id="d10ef-127">**Failure Audit**</span></span> | <span data-ttu-id="d10ef-128">Событие, записывающее попытку безопасного доступа, которая завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d10ef-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="d10ef-129">Например, если пользователь пытается получить доступ к сетевому диску и происходит сбой, попытка регистрируется как событие неудачного аудита.</span><span class="sxs-lookup"><span data-stu-id="d10ef-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="d10ef-130">Выбранные действия пользователей могут отслеживаться с помощью аудита событий безопасности и последующего размещения записей в журнале безопасности компьютера.</span><span class="sxs-lookup"><span data-stu-id="d10ef-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



