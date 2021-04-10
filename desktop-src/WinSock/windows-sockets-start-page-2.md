---
description: Сокеты Windows 2 (Winsock) позволяют программистам создавать расширенные Интернет, интрасети и другие сетевые приложения для передачи данных приложений по сети независимо от используемого сетевого протокола.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Сокеты Windows 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155255"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="06a29-103">Сокеты Windows 2</span><span class="sxs-lookup"><span data-stu-id="06a29-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="06a29-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="06a29-104">Purpose</span></span>

<span data-ttu-id="06a29-105">Сокеты Windows 2 (Winsock) позволяют программистам создавать расширенные Интернет, интрасети и другие сетевые приложения для передачи данных приложений по сети независимо от используемого сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="06a29-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="06a29-106">С помощью Winsock программисты получают доступ к расширенным возможностям Microsoft® Windows® сетевые возможности, такие как многоадресная рассылка и качество обслуживания (QoS).</span><span class="sxs-lookup"><span data-stu-id="06a29-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="06a29-107">Winsock соответствует модели архитектуры Windows Open System (ВОСА). Он определяет стандартный интерфейс поставщика услуг (SPI) между прикладным программным интерфейсом (API), его экспортированными функциями и стеками протоколов.</span><span class="sxs-lookup"><span data-stu-id="06a29-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="06a29-108">Он использует парадигму сокетов, которая была впервые популярна с помощью Berkeley Software Distribution (BSD) UNIX.</span><span class="sxs-lookup"><span data-stu-id="06a29-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="06a29-109">Это было впоследствии адаптировано для Windows в Windows Sockets 1,1, с которым приложения Windows Sockets 2 являются обратно совместимыми.</span><span class="sxs-lookup"><span data-stu-id="06a29-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="06a29-110">Программное обеспечение Winsock, ранее выровненное по протоколу TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="06a29-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="06a29-111">Некоторые методы программирования, которые работали с TCP/IP, не работают с каждым протоколом.</span><span class="sxs-lookup"><span data-stu-id="06a29-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="06a29-112">В результате API-интерфейс сокетов Windows 2 добавляет функции, необходимые для работы с несколькими протоколами.</span><span class="sxs-lookup"><span data-stu-id="06a29-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="06a29-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="06a29-113">Developer audience</span></span>

<span data-ttu-id="06a29-114">Сокеты Windows 2 предназначены для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="06a29-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="06a29-115">Вам потребуются навыки работы с сетью Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="06a29-116">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="06a29-116">Run-time requirements</span></span>

<span data-ttu-id="06a29-117">Сокеты Windows 2 можно использовать на всех платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="06a29-118">Если существуют определенные реализации или возможности ограничений платформы Windows Sockets 2, они четко отмечены в документации.</span><span class="sxs-lookup"><span data-stu-id="06a29-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06a29-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="06a29-119">In this section</span></span>



| <span data-ttu-id="06a29-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="06a29-120">Topic</span></span>                                                                                             | <span data-ttu-id="06a29-121">Описание</span><span class="sxs-lookup"><span data-stu-id="06a29-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06a29-122">Новые возможности в сокетах Windows</span><span class="sxs-lookup"><span data-stu-id="06a29-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="06a29-123">Сведения о новых возможностях для сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="06a29-124">Поддержка сетевого протокола Winsock в Windows</span><span class="sxs-lookup"><span data-stu-id="06a29-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="06a29-125">Сведения о поддержке сетевого протокола для сокетов Windows в различных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="06a29-126">Об Winsock</span><span class="sxs-lookup"><span data-stu-id="06a29-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="06a29-127">Общие сведения о вопросах программирования, архитектуре и возможностях, предоставляемых разработчикам Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="06a29-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="06a29-128">Использование Winsock</span><span class="sxs-lookup"><span data-stu-id="06a29-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="06a29-129">Процедуры и методы программирования, используемые с сокетами Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="06a29-130">В этом разделе приводятся основные методики программирования Winsock, такие как [Начало работы с Winsock](getting-started-with-winsock.md), а также расширенные методики, полезные для опытных разработчиков Winsock.</span><span class="sxs-lookup"><span data-stu-id="06a29-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="06a29-131">Справочник по Winsock</span><span class="sxs-lookup"><span data-stu-id="06a29-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="06a29-132">Документация по API-интерфейсу сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="06a29-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="06a29-133">См. также</span><span class="sxs-lookup"><span data-stu-id="06a29-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a29-134">Вспомогательная служба IP</span><span class="sxs-lookup"><span data-stu-id="06a29-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="06a29-135">Качество обслуживания</span><span class="sxs-lookup"><span data-stu-id="06a29-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
