---
title: Использование элемента управления ActiveX удаленный рабочий стол с виртуальными каналами
description: Если вы включили приложение виртуальных каналов в развертывание службы удаленных рабочих столов, это приложение можно будет сделать доступным для клиентских компьютеров.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888524"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="34b70-103">Использование элемента управления ActiveX удаленный рабочий стол с виртуальными каналами</span><span class="sxs-lookup"><span data-stu-id="34b70-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="34b70-104">Если вы включили приложение виртуальных каналов в развертывание службы удаленных рабочих столов, это приложение можно сделать доступным для клиентских компьютеров, которые обращаются к серверу узла сеансов удаленный рабочий стол (сервер узла сеансов удаленных рабочих столов) с помощью удаленный рабочий стол элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="34b70-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="34b70-105">**Предоставление доступа к приложению виртуального канала**</span><span class="sxs-lookup"><span data-stu-id="34b70-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="34b70-106">Разверните серверный модуль приложения и убедитесь, что он выполняется на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="34b70-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="34b70-107">На странице Подключение веб-приложения службы удаленных рабочих столов, работающего на веб-сервере, обратитесь к свойству **плугиндллс** интерфейса [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) , чтобы указать имя библиотеки DLL виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="34b70-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="34b70-108">При наличии нескольких подключаемых модулей укажите имена библиотек DLL с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="34b70-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="34b70-109">Например, если подключаемый модуль виртуального канала имеет имя "MyPlugin.dll", используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="34b70-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="34b70-110">Используйте следующий код, если у вас есть две библиотеки DLL виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="34b70-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="34b70-111">В этом примере имена файлов DLL имеют значение "MyPlugin.dll" и "Vdriver.dll":</span><span class="sxs-lookup"><span data-stu-id="34b70-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="34b70-112">По соображениям безопасности свойство **плугиндллс** принимает только именованный список библиотек DLL виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="34b70-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="34b70-113">Элемент управления возвращает ошибку, если указана любая форма файловой системы или путь в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="34b70-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="34b70-114">Кроме того, имена библиотек DLL должны содержать только алфавитно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="34b70-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="34b70-115">Убедитесь, что клиентский модуль установлен в каталоге% WINDIR% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="34b70-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="34b70-116">API виртуальных каналов не допускает загрузку нескольких экземпляров одной и той же библиотеки виртуальных каналов в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="34b70-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="34b70-117">В связи с этим при наличии нескольких экземпляров элемента управления ActiveX удаленный рабочий стол, выполняющихся в одном процессе, только первый экземпляр элемента управления сможет загрузить библиотеку DLL виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="34b70-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="34b70-118">Если вы разрабатываете приложение виртуального канала, которое должно поддерживать несколько экземпляров в рамках одного процесса, для реализации приложения виртуального канала необходимо использовать API [динамических виртуальных каналов](dynamic-virtual-channels.md) .</span><span class="sxs-lookup"><span data-stu-id="34b70-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="34b70-119">По умолчанию удаленный рабочий стол элемент управления ActiveX загружает клиентские библиотеки DLL виртуальных каналов из каталога% WINDIR% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="34b70-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="34b70-120">Администратор может изменить каталог DLL подключаемого модуля клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34b70-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="34b70-121">Чтобы сделать это, измените раздел реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **терминалов Client** \\ **вдллпас** на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="34b70-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="34b70-122">Путь к каталогу не может быть указан в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="34b70-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




