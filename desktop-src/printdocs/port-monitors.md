---
description: После того как драйвер устройства преобразует весь файл журнала в команды необработанного устройства, файл преобразованных команд передается обратно в Диспетчер очереди печати.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Мониторы портов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702545"
---
# <a name="port-monitors"></a><span data-ttu-id="0e5e0-103">Мониторы портов</span><span class="sxs-lookup"><span data-stu-id="0e5e0-103">Port Monitors</span></span>

<span data-ttu-id="0e5e0-104">После того как драйвер устройства преобразует весь файл журнала в команды необработанного устройства, файл преобразованных команд передается обратно в Диспетчер очереди печати.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="0e5e0-105">Диспетчер очереди отправки команд низкого уровня в монитор.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="0e5e0-106">Монитор порта — это библиотека DLL, которая передает команды необработанного устройства по сети, через параллельный порт или через последовательный порт на устройство принтера.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="0e5e0-107">Для поддержки передачи данных устройства через другие порты связи можно установить настраиваемые мониторы портов.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="0e5e0-108">Используйте следующие функции для работы с мониторами портов.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="0e5e0-109">Функция</span><span class="sxs-lookup"><span data-stu-id="0e5e0-109">Function</span></span>                               | <span data-ttu-id="0e5e0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e5e0-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e5e0-111">**аддмонитор**</span><span class="sxs-lookup"><span data-stu-id="0e5e0-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="0e5e0-112">Устанавливает монитор локального порта и связывает файлы конфигурации, данных и монитора.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="0e5e0-113">**делетемонитор**</span><span class="sxs-lookup"><span data-stu-id="0e5e0-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="0e5e0-114">Удаляет монитор портов, добавленный функцией [**аддмонитор**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5e0-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="0e5e0-115">**енуммониторс**</span><span class="sxs-lookup"><span data-stu-id="0e5e0-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="0e5e0-116">Перечисление мониторов портов, установленных на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="0e5e0-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



