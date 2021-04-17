---
description: Одной из основных функций функций в API печати GDI является поддержка независимости устройства.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Сведения об API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693423"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="73e7c-103">Сведения об API печати GDI</span><span class="sxs-lookup"><span data-stu-id="73e7c-103">About the GDI Print API</span></span>

<span data-ttu-id="73e7c-104">Одной из основных функций функций в API печати GDI является поддержка независимости устройства.</span><span class="sxs-lookup"><span data-stu-id="73e7c-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="73e7c-105">Вместо выдачи команд для конкретного устройства для вывода выходных данных на определенном принтере или плоттере приложение вызывает функции высокого уровня из интерфейса графических устройств (GDI).</span><span class="sxs-lookup"><span data-stu-id="73e7c-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="73e7c-106">Например, чтобы напечатать растровое изображение, приложение может вызвать функцию [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , указав координаты точечного рисунка, а также дескрипторы, определяющие контексты исходного и целевого устройств (DCS).</span><span class="sxs-lookup"><span data-stu-id="73e7c-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="73e7c-107">После этого вызов **BitBlt** преобразуется в команды необработанного устройства драйвером принтера.</span><span class="sxs-lookup"><span data-stu-id="73e7c-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="73e7c-108">Драйвер устройства — это библиотека динамической компоновки (DLL), которая поддерживает интерфейс драйвера устройства (DDI).</span><span class="sxs-lookup"><span data-stu-id="73e7c-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="73e7c-109">Драйвер устройства создает команды необработанных устройств при обработке вызовов функций DDI, выполненных модулем обработки графики.</span><span class="sxs-lookup"><span data-stu-id="73e7c-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="73e7c-110">Команды обрабатываются принтером при печати изображения.</span><span class="sxs-lookup"><span data-stu-id="73e7c-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="73e7c-111">Синтаксис, число и тип этих команд отличаются от устройства к устройству.</span><span class="sxs-lookup"><span data-stu-id="73e7c-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="73e7c-112">В этом обзоре содержатся сведения по следующим темам.</span><span class="sxs-lookup"><span data-stu-id="73e7c-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="73e7c-113">Интерфейс печати по умолчанию</span><span class="sxs-lookup"><span data-stu-id="73e7c-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="73e7c-114">Контексты печатающих устройств</span><span class="sxs-lookup"><span data-stu-id="73e7c-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="73e7c-115">Escape-последовательности принтера</span><span class="sxs-lookup"><span data-stu-id="73e7c-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="73e7c-116">Отображение и вывод WYSIWYG</span><span class="sxs-lookup"><span data-stu-id="73e7c-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="73e7c-117">DEVMODE для каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="73e7c-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
