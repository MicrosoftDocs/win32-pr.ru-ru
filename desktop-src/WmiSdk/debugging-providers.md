---
description: Поставщики, если они не являются разъединенными поставщиками, работающими в приложении, загружаются в Wmiprvse.exe процесс, а не в Svchost.exe с Winmgmt.exeным процессом. Дополнительные сведения см. в разделе Размещение и безопасность поставщика.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Отладка поставщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991565"
---
# <a name="debugging-providers"></a><span data-ttu-id="13fdc-104">Отладка поставщиков</span><span class="sxs-lookup"><span data-stu-id="13fdc-104">Debugging Providers</span></span>

<span data-ttu-id="13fdc-105">Поставщики, если они не являются [*разъединенными поставщиками*](gloss-d.md) , работающими в приложении, загружаются в Wmiprvse.exe процесс, а не в Svchost.exe с Winmgmt.exeным процессом.</span><span class="sxs-lookup"><span data-stu-id="13fdc-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="13fdc-106">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="13fdc-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="13fdc-107">При остановке в точке останова отладчик Visual Studio замораживает весь ведущий процесс поставщика, который обычно является Wmiprvse.exeом общего узла.</span><span class="sxs-lookup"><span data-stu-id="13fdc-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="13fdc-108">Это предотвращает работу любых других компонентов, размещенных в этом процессе, включая расширение WMI обозреватель сервера.</span><span class="sxs-lookup"><span data-stu-id="13fdc-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="13fdc-109">Клиентские приложения, которые вызывают поставщик, также блокируются.</span><span class="sxs-lookup"><span data-stu-id="13fdc-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="13fdc-110">В Windows 2000 и более ранних проблемах возникают проблемы, поскольку поставщик загружается в процесс службы WMI (Winmgmt.exe).</span><span class="sxs-lookup"><span data-stu-id="13fdc-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="13fdc-111">Если вы запускаете WMI обозреватель сервера в другом экземпляре, интегрированная среда разработки Visual Studio не зависает и вы можете освободить точку останова.</span><span class="sxs-lookup"><span data-stu-id="13fdc-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="13fdc-112">Рекомендуется запускать поставщик в отдельном ведущем процессе на этапе разработки, чтобы остановка в точке останова замораживает только процесс, в котором размещен поставщик.</span><span class="sxs-lookup"><span data-stu-id="13fdc-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="13fdc-113">Другие функции WMI по-прежнему доступны для обозреватель сервера WMI и любых других приложений или скриптов на основе WMI.</span><span class="sxs-lookup"><span data-stu-id="13fdc-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="13fdc-114">Кроме того, если поставщик аварийно завершает работу, он не влияет на работу других поставщиков, загруженных в тот же ведущий процесс.</span><span class="sxs-lookup"><span data-stu-id="13fdc-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="13fdc-115">Чтобы обеспечить загрузку поставщика в собственном хосте процесса, измените регистрацию поставщика, чтобы задать для свойства [**\_ \_ Win32Provider. хостингмодел**](--win32provider.md) значение `NetworkServiceHost:[MyProvider]` , где мипровидер может быть любой строкой, однозначно идентифицирующей поставщик.</span><span class="sxs-lookup"><span data-stu-id="13fdc-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="13fdc-116">Например, используйте значение **\_ \_ Win32Provider. CLSID** .</span><span class="sxs-lookup"><span data-stu-id="13fdc-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="13fdc-117">Когда поставщик готов к отправке, возвратите **\_ \_ Win32Provider. хостингмодел** к предполагаемому значению, например **нетворксервицехост**.</span><span class="sxs-lookup"><span data-stu-id="13fdc-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="13fdc-118">Если отладка поставщика не выполняется, можно вызвать [**метод Load \_ класса поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) , чтобы принудительно загрузить поставщик, а затем присоединиться к Wmiprvse.exe процессу с загруженной библиотекой DLL и выполнить отладку по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="13fdc-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13fdc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="13fdc-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="13fdc-120">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="13fdc-120">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="13fdc-121">Классы устранения неполадок WMI</span><span class="sxs-lookup"><span data-stu-id="13fdc-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
