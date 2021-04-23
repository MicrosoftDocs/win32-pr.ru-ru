---
description: В состав Windows SDK для Windows Server 2008 входит два примера WSDAPI.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Примеры WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812370"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="ed34b-103">Примеры WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ed34b-103">WSDAPI Samples</span></span>

<span data-ttu-id="ed34b-104">В состав Windows SDK для Windows Server 2008 входит два примера WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ed34b-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="ed34b-105">Исходный код для образцов можно найти в <Windows SDK Install Folder> \\ примерах \\ веб- \\ WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ed34b-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="ed34b-106">Эта версия пакета SDK доступна в [центре загрузки](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="ed34b-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="ed34b-107">Образцы недоступны в пакете SDK для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed34b-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="ed34b-108">Образец котировки котировок (расположенный в <Windows SDK Install Folder> \\ примерах \\ Web \\ WSDAPI \\ стокккуоте) демонстрирует службу с базовой функциональностью обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ed34b-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="ed34b-109">Пример службы файлов (расположенный в <Windows SDK Install Folder> \\ примерах \\ Web \\ WSDAPI \\ FileService) демонстрирует службу с расширенными функциями, такими как асинхронный обмен сообщениями, вложения и события.</span><span class="sxs-lookup"><span data-stu-id="ed34b-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="ed34b-110">Оба образца включают следующие типы файлов.</span><span class="sxs-lookup"><span data-stu-id="ed34b-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="ed34b-111">WSDL-файлы, содержащие описания служб.</span><span class="sxs-lookup"><span data-stu-id="ed34b-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="ed34b-112">[Файлы конфигурации всдкодежен](wsdcodegen-configuration-file.md) , используемые для создания кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ed34b-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="ed34b-113">Созданный заголовок и исходные файлы C++.</span><span class="sxs-lookup"><span data-stu-id="ed34b-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="ed34b-114">Файлы реализации клиента и службы.</span><span class="sxs-lookup"><span data-stu-id="ed34b-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="ed34b-115">Файлы проекта и решения Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ed34b-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="ed34b-116">Оба примера реализуют узлы устройств ([**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), прокси-серверы устройств ([**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) и прокси-серверы служб ([**ивсдсервицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="ed34b-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="ed34b-117">Кроме того, в примере службы файлов демонстрируется использование асинхронного обмена сообщениями ([**ивсдасинккаллбакк**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**ивсдасинкресулт**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), вложений ([**ивсдинбаундаттачмент**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**ивсдаутбаундаттачмент**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) и событий.</span><span class="sxs-lookup"><span data-stu-id="ed34b-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="ed34b-118">Файлы Филесервицеконтракт. vcproj и Стокккуотеконтракт. vcproj, содержащиеся в примерах, вызывают [всдкодежен](web-services-for-devices-code-generator.md) для создания заголовка и исходных файлов C++ из WSDL-файла, указанного в файле конфигурации всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="ed34b-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="ed34b-119">Это означает, что при изменении образца файла конфигурации WSDL или Всдкодежен и перестроении примера проекта Всдкодежен автоматически создает новые заголовочные и исходные файлы, отражающие изменения.</span><span class="sxs-lookup"><span data-stu-id="ed34b-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="ed34b-120">Это предпочтительный метод создания приложений WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ed34b-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="ed34b-121">Всдкодежен обычно вызывается из командной строки.</span><span class="sxs-lookup"><span data-stu-id="ed34b-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="ed34b-122">Откройте соответствующий \* файл. vcproj, чтобы просмотреть пример вызовов командной строки всдкодежен.</span><span class="sxs-lookup"><span data-stu-id="ed34b-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed34b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ed34b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed34b-124">Разработка приложений WSD в Windows</span><span class="sxs-lookup"><span data-stu-id="ed34b-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



