---
description: Windows GDI+ — это подсистема операционной системы Windows XP или Windows Server 2003, которая отвечает за отображение информации на экранах и принтерах. GDI+ — это API, предоставляемый через набор классов C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Общие сведения о GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997462"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="53df0-104">Общие сведения о GDI+</span><span class="sxs-lookup"><span data-stu-id="53df0-104">Overview of GDI+</span></span>

<span data-ttu-id="53df0-105">Windows GDI+ — это подсистема операционной системы Windows XP или Windows Server 2003, которая отвечает за отображение информации на экранах и принтерах.</span><span class="sxs-lookup"><span data-stu-id="53df0-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="53df0-106">GDI+ — это API, предоставляемый через набор классов C++.</span><span class="sxs-lookup"><span data-stu-id="53df0-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="53df0-107">Как видно из названия, GDI+ является преемником Windows интерфейс графических устройств (GDI), интерфейсом графических устройств, включенным в более ранние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="53df0-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="53df0-108">Windows XP или Windows Server 2003 поддерживает GDI для совместимости с существующими приложениями, но программисты новых приложений должны использовать GDI+ для всех своих графических нужд, так как GDI+ оптимизирует многие возможности GDI, а также предоставляет дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="53df0-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="53df0-109">Интерфейс графических устройств, например GDI+, позволяет программистам приложений отображать информацию на экране или принтере без необходимости беспокоиться о деталях конкретного устройства отображения.</span><span class="sxs-lookup"><span data-stu-id="53df0-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="53df0-110">Программист приложения обращается к методам, предоставляемым классами GDI+, и эти методы, в свою очередь, выполняют соответствующие вызовы конкретных драйверов устройств.</span><span class="sxs-lookup"><span data-stu-id="53df0-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="53df0-111">GDI+ изолирует приложение от графического оборудования, и это изоляция, позволяющая разработчикам создавать приложения, независимые от устройств.</span><span class="sxs-lookup"><span data-stu-id="53df0-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



