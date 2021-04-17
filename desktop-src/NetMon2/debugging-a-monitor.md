---
description: В следующей процедуре показано, как выполнить отладку монитора.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Отладка монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545383"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="698e3-103">Отладка монитора</span><span class="sxs-lookup"><span data-stu-id="698e3-103">Debugging a Monitor</span></span>

<span data-ttu-id="698e3-104">В следующей процедуре показано, как выполнить отладку монитора.</span><span class="sxs-lookup"><span data-stu-id="698e3-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="698e3-105">**Отладка монитора**</span><span class="sxs-lookup"><span data-stu-id="698e3-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="698e3-106">Установите DLL монитора и файл базы данных программы (. pdb), созданный при компиляции монитора в нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="698e3-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="698e3-107">Дополнительные сведения см. [в разделе Установка монитора в сетевой монитор](installing-a-monitor-to-network-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="698e3-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="698e3-108">Убедитесь, что служба управления монитором настроена как сервер, а не как служба, выбрав Панель управления, службы.</span><span class="sxs-lookup"><span data-stu-id="698e3-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="698e3-109">Откройте командную строку и перейдите в каталог сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="698e3-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="698e3-110">Тип:</span><span class="sxs-lookup"><span data-stu-id="698e3-110">Type:</span></span>

    <span data-ttu-id="698e3-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="698e3-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="698e3-112">После завершения сеанса отладки монитора можно вернуть МКСВК к его условию по умолчанию, введя:</span><span class="sxs-lookup"><span data-stu-id="698e3-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="698e3-113">**Mcsvc.exe свойством/Service**</span><span class="sxs-lookup"><span data-stu-id="698e3-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="698e3-114">В Microsoft Visual Studio запустите Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="698e3-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="698e3-115">В меню **файл** выберите пункт **Открыть** , а затем выберите имя библиотеки DLL монитора.</span><span class="sxs-lookup"><span data-stu-id="698e3-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="698e3-116">После загрузки Microsoft Visual C++ щелкните **проект**, **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="698e3-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="698e3-117">Перейдите на вкладку **Отладка** в разделе **исполняемый файл** для сеанса отладки и введите полный путь к Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="698e3-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="698e3-118">Например, C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="698e3-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="698e3-119">Задайте точки останова в коде.</span><span class="sxs-lookup"><span data-stu-id="698e3-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="698e3-120">Не используйте окно сообщения для отслеживания отладки.</span><span class="sxs-lookup"><span data-stu-id="698e3-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="698e3-121">Если МКСВК работает как служба, всплывающее окно не появится, и МКСВК будет выглядеть под зависание.</span><span class="sxs-lookup"><span data-stu-id="698e3-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



