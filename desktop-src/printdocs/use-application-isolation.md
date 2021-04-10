---
description: Приложения могут объявлять изоляцию драйвера принтера в манифесте приложения, чтобы изолировать приложение от драйвера принтера и повысить надежность приложений.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: Как использовать изоляцию приложений
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264444"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="f0364-103">Как использовать изоляцию приложений</span><span class="sxs-lookup"><span data-stu-id="f0364-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="f0364-104">Приложения могут объявлять изоляцию драйвера принтера в манифесте приложения, чтобы изолировать приложение от драйвера принтера и повысить надежность приложения.</span><span class="sxs-lookup"><span data-stu-id="f0364-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="f0364-105">Служба печати Windows позволяет запускать драйверы принтеров в процессах, отдельных от процесса, в котором работает диспетчер очереди печати.</span><span class="sxs-lookup"><span data-stu-id="f0364-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="f0364-106">С помощью этой функции приложение предотвращает его аварийное завершение в случае возникновения ошибки в драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="f0364-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="f0364-107">Изоляция драйвера принтера реализована в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f0364-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f0364-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f0364-108">Prerequisites</span></span>

-   <span data-ttu-id="f0364-109">Управляемый код или приложение Магазина Windows, использующее печать Windows.</span><span class="sxs-lookup"><span data-stu-id="f0364-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="f0364-110">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f0364-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="f0364-111">Обновление манифеста приложения</span><span class="sxs-lookup"><span data-stu-id="f0364-111">Update the app manifest</span></span>

<span data-ttu-id="f0364-112">Включение изоляции драйвера принтера требует добавления элемента **принтердриверисолатион** в манифест приложения.</span><span class="sxs-lookup"><span data-stu-id="f0364-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="f0364-113">Вот как это сделать.</span><span class="sxs-lookup"><span data-stu-id="f0364-113">Here's how:</span></span>

1.  <span data-ttu-id="f0364-114">Измените манифест приложения, добавив элемент **принтердриверисолатион** со значением **true** в элемент **виндовссеттингс** элемента **Application** , как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="f0364-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="f0364-115">Перестройте приложение.</span><span class="sxs-lookup"><span data-stu-id="f0364-115">Rebuild your app.</span></span>

 

 



