---
title: Подключаемые модули пользовательского интерфейса проигрывателя Windows Media
description: Подключаемые модули пользовательского интерфейса проигрывателя Windows Media
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Проигрыватель Windows Media, подключаемые модули
- Проигрыватель Windows Media, подключаемые модули пользовательского интерфейса
- Подключаемые модули проигрывателя Windows Media, Пользовательский интерфейс
- подключаемые модули, Пользовательский интерфейс
- подключаемые модули пользовательского интерфейса, сведения
- Сведения о подключаемых модулях пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700527"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="80d20-109">Подключаемые модули пользовательского интерфейса проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="80d20-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="80d20-110">Проигрыватель Microsoft Windows Media предоставляет архитектуру, позволяющую пользователю устанавливать и активировать подключаемые программы, которые добавляют функциональные возможности пользовательского интерфейса в полный режим проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="80d20-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="80d20-111">Типичный подключаемый модуль пользовательского интерфейса может позволить пользователю купить компакт-диск, содержащий текущую воспроизводимую запись, или получить доступ к дополнительным сведениям об исполнителе.</span><span class="sxs-lookup"><span data-stu-id="80d20-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="80d20-112">В этом разделе пакета средств разработки программного обеспечения (SDK) проигрывателя Windows Media содержатся сведения о программировании, необходимые для создания собственного подключаемого модуля пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80d20-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="80d20-113">Документация по подключаемому модулю пользовательского интерфейса делится на три раздела:</span><span class="sxs-lookup"><span data-stu-id="80d20-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="80d20-114">Section</span><span class="sxs-lookup"><span data-stu-id="80d20-114">Section</span></span>                                                                                            | <span data-ttu-id="80d20-115">Описание</span><span class="sxs-lookup"><span data-stu-id="80d20-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80d20-116">О подключаемых модулях пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="80d20-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="80d20-117">Содержит общие сведения об архитектуре, используемой для подключаемых модулей пользовательского интерфейса. Ознакомьтесь с этим разделом, чтобы узнать об общих принципах, связанных с этой технологией.</span><span class="sxs-lookup"><span data-stu-id="80d20-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="80d20-118">Программное руководством по программированию подключаемых модулей пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="80d20-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="80d20-119">Объясняет, что необходимо сделать для создания подключаемого модуля пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80d20-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="80d20-120">Этот раздел содержит пример кода и пошаговые процедуры.</span><span class="sxs-lookup"><span data-stu-id="80d20-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="80d20-121">Справочник по программированию подключаемых модулей пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="80d20-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="80d20-122">Содержит подробный справочник по COM-интерфейсу и методам, поддерживаемым пакетом SDK проигрывателя Windows Media для подключаемых модулей пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80d20-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="80d20-123">Проигрыватель Windows Media 10 Mobile предоставляет ту же модель подключаемых модулей, что и классическое устройство Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="80d20-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="80d20-124">Эта модель подключаемых модулей позволяет использовать фоновые подключаемые модули для мониторинга событий, отображения состояния свойств и т. д.</span><span class="sxs-lookup"><span data-stu-id="80d20-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="80d20-125">В этом разделе описано, как создать фоновый подключаемый модуль пользовательского интерфейса для проигрывателя Windows Media 10 Mobile с помощью мастера подключаемого модуля проигрывателя Windows Media для настольных систем.</span><span class="sxs-lookup"><span data-stu-id="80d20-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="80d20-126">См. также</span><span class="sxs-lookup"><span data-stu-id="80d20-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d20-127">**Подключаемые модули проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="80d20-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




