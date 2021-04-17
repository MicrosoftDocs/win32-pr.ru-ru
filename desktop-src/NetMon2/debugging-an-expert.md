---
description: Используйте следующую процедуру для отладки экспертов, написанных на Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Отладка эксперта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663640"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="521ee-103">Отладка эксперта</span><span class="sxs-lookup"><span data-stu-id="521ee-103">Debugging an Expert</span></span>

<span data-ttu-id="521ee-104">Используйте следующую процедуру для отладки экспертов, написанных на Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="521ee-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="521ee-105">**Отладка эксперта**</span><span class="sxs-lookup"><span data-stu-id="521ee-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="521ee-106">Установите эксперт (DLL-файл) и файл базы данных программы (. pdb), созданный при компиляции эксперта в нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="521ee-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="521ee-107">Дополнительные сведения см. [в статье Установка эксперта в сетевой монитор 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="521ee-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="521ee-108">Запустите Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="521ee-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="521ee-109">В меню **файл** щелкните **Открыть** и выберите имя библиотеки DLL эксперта.</span><span class="sxs-lookup"><span data-stu-id="521ee-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="521ee-110">После загрузки Microsoft Visual C++ в меню **проект** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="521ee-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="521ee-111">Нажмите кнопку **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="521ee-111">Click **Debug**.</span></span> <span data-ttu-id="521ee-112">В разделе **исполняемый файл для сеанса отладки** введите полный путь к Netmon.exe, например:</span><span class="sxs-lookup"><span data-stu-id="521ee-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="521ee-113">Задайте точки останова в коде.</span><span class="sxs-lookup"><span data-stu-id="521ee-113">Set the breakpoints in your code.</span></span>

 

 



