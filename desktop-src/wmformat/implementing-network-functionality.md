---
title: Реализация функций сети
description: Реализация функций сети
ms.assetid: 908e269b-63be-4666-a364-a894f6dcd86f
keywords:
- Windows Media Format SDK, реализация функций сети
- Windows Media Format SDK, сетевые функции
- Расширенный системный формат (ASF), реализация функций сети
- ASF (Расширенный системный формат), реализация функций сети
- Расширенный системный формат (ASF), сетевая функциональность
- ASF (Расширенный системный формат), сетевые функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631b6a322293bffe71ce92afcb684901cc60d16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532375"
---
# <a name="implementing-network-functionality"></a><span data-ttu-id="8eb5b-109">Реализация функций сети</span><span class="sxs-lookup"><span data-stu-id="8eb5b-109">Implementing Network Functionality</span></span>

<span data-ttu-id="8eb5b-110">В этом разделе описывается, как использовать сетевые функции, доступные в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-110">This section describes how to use the networking features available through the Windows Media Format SDK.</span></span> <span data-ttu-id="8eb5b-111">Приложение может использовать эти функции для чтения потоков ASF из сети, вещания потоков ASF в сеть или отправки ASF-потоков в точку публикации на сервере, на котором работают службы Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-111">An application can use these features to read ASF streams from a network, broadcast ASF streams to a network, or push ASF streams to a publishing point on a server running Windows Media Services.</span></span>

<span data-ttu-id="8eb5b-112">В следующих разделах описываются сетевые возможности этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-112">The following sections describe the networking features of this SDK.</span></span>



| <span data-ttu-id="8eb5b-113">Section</span><span class="sxs-lookup"><span data-stu-id="8eb5b-113">Section</span></span>                                                                    | <span data-ttu-id="8eb5b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8eb5b-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8eb5b-115">Обзор сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="8eb5b-115">Overview of Networking Interfaces</span></span>](overview-of-networking-interfaces.md) | <span data-ttu-id="8eb5b-116">Имена и описание каждого интерфейса, поддерживающего сетевые методы.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-116">Names and describes each interface that supports networking methods.</span></span>                                                 |
| [<span data-ttu-id="8eb5b-117">Чтение данных ASF по сети</span><span class="sxs-lookup"><span data-stu-id="8eb5b-117">Reading ASF Data Over a Network</span></span>](reading-asf-data-over-a-network.md)     | <span data-ttu-id="8eb5b-118">Описывает, как воспроизводить файлы из источника сети и как настроить параметры сети для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-118">Describes how to play files from a network source and how to configure the network settings on the reader object.</span></span>    |
| [<span data-ttu-id="8eb5b-119">Отправка данных ASF по сети</span><span class="sxs-lookup"><span data-stu-id="8eb5b-119">Sending ASF Data Over a Network</span></span>](sending-asf-data-over-a-network.md)     | <span data-ttu-id="8eb5b-120">Описывает, как рассылать данные ASF по сети или передавать данные ASF в точку публикации на сервере Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-120">Describes how to broadcast ASF data over a network or send ASF data to a publishing point on a Windows Media server.</span></span> |
| [<span data-ttu-id="8eb5b-121">Параметры сети по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8eb5b-121">Default Networking Settings</span></span>](default-networking-settings.md)             | <span data-ttu-id="8eb5b-122">Содержит краткий справочник по параметрам по умолчанию, используемым пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="8eb5b-122">Provides a quick reference for the default settings used by the SDK.</span></span>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="8eb5b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8eb5b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb5b-124">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="8eb5b-124">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




