---
description: Контроллер домена может использоваться при печати на матричном принтере, на принтере с рукописным вводом, на лазерном принтере или плоттере.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Контексты печатающих устройств (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984853"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="6421d-103">Контексты печатающих устройств (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="6421d-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="6421d-104">Контроллер домена может использоваться при печати на матричном принтере, на принтере с рукописным вводом, на лазерном принтере или плоттере.</span><span class="sxs-lookup"><span data-stu-id="6421d-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="6421d-105">Приложение создает контроллер домена, вызывая функцию [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) и предоставляя соответствующие аргументы (имя драйвера принтера, имя принтера, имя файла или устройства для физического выходного носителя и другие данные инициализации).</span><span class="sxs-lookup"><span data-stu-id="6421d-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="6421d-106">После завершения печати приложения он удаляет контроллер домена, вызывая функцию [**делетедк**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="6421d-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="6421d-107">Приложение должно удалять (а не выпустить) контроллер домена принтера; Функция [**релеаседк**](/windows/desktop/api/Winuser/nf-winuser-releasedc) завершается ошибкой, когда приложение пытается использовать его для выпуска контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="6421d-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="6421d-108">Дополнительные сведения см. в разделе [вывод принтера](../printdocs/printer-output.md).</span><span class="sxs-lookup"><span data-stu-id="6421d-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
