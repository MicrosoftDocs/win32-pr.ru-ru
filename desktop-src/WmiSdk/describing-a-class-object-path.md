---
description: Путь к объекту класса описывает расположение класса в пространстве имен.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Описание пути к объекту класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702720"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="0daf9-103">Описание пути к объекту класса</span><span class="sxs-lookup"><span data-stu-id="0daf9-103">Describing a Class Object Path</span></span>

<span data-ttu-id="0daf9-104">Путь к объекту класса описывает расположение класса в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0daf9-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="0daf9-105">Для указания пути к объекту можно использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="0daf9-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="0daf9-106">Полный путь к объекту класса добавляет имя класса к пути к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="0daf9-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="0daf9-107">В следующем примере показано расположение класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в \\ корневом \\ пространстве имен CIMV2 на сервере с именем admin.</span><span class="sxs-lookup"><span data-stu-id="0daf9-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="0daf9-108">Относительный путь к объекту представляет класс, находящийся в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0daf9-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="0daf9-109">Относительный путь к объекту класса содержит только имя класса.</span><span class="sxs-lookup"><span data-stu-id="0daf9-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="0daf9-110">В следующем примере показан относительный путь к классу [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="0daf9-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="0daf9-111">При запросе имени класса без указания экземпляров Инструментарий WMI возвращает определение класса.</span><span class="sxs-lookup"><span data-stu-id="0daf9-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="0daf9-112">Следующая процедура описывает, как получить определение класса в VBScript.</span><span class="sxs-lookup"><span data-stu-id="0daf9-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="0daf9-113">**Извлечение определения класса в VBScript**</span><span class="sxs-lookup"><span data-stu-id="0daf9-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="0daf9-114">Подключение моникера можно использовать с запросом или [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="0daf9-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="0daf9-115">Можно также использовать [**SwbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="0daf9-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="0daf9-116">В следующем примере показано, как использовать [GetObject](/previous-versions//kdccchxa(v=vs.85)) для получения определения класса.</span><span class="sxs-lookup"><span data-stu-id="0daf9-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="0daf9-117">В следующем примере показано, как запросить определение класса.</span><span class="sxs-lookup"><span data-stu-id="0daf9-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="0daf9-118">Определение класса в C++ можно получить, указав только имя класса и путь к конкретному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="0daf9-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="0daf9-119">В следующей процедуре описывается извлечение определения класса в C++.</span><span class="sxs-lookup"><span data-stu-id="0daf9-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="0daf9-120">**Извлечение определения класса в C++**</span><span class="sxs-lookup"><span data-stu-id="0daf9-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="0daf9-121">Выполните вызов функций [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="0daf9-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="0daf9-122">В следующем примере показано, как вызвать функцию [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="0daf9-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="0daf9-123">В предыдущем примере кода \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="0daf9-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
