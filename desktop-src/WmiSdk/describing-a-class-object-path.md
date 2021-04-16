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
# <a name="describing-a-class-object-path"></a>Описание пути к объекту класса

Путь к объекту класса описывает расположение класса в пространстве имен.

Для указания пути к объекту можно использовать следующие методы:

-   Полный путь к объекту класса добавляет имя класса к пути к пространству имен.

    В следующем примере показано расположение класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в \\ корневом \\ пространстве имен CIMV2 на сервере с именем admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Относительный путь к объекту представляет класс, находящийся в текущем пространстве имен. Относительный путь к объекту класса содержит только имя класса.

    В следующем примере показан относительный путь к классу [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

    ``` syntax
    Win32_LogicalDisk
    ```

При запросе имени класса без указания экземпляров Инструментарий WMI возвращает определение класса. Следующая процедура описывает, как получить определение класса в VBScript.

**Извлечение определения класса в VBScript**

-   Подключение моникера можно использовать с запросом или [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). Можно также использовать [**SwbemServices. Get**](swbemservices-get.md).

    В следующем примере показано, как использовать [GetObject](/previous-versions//kdccchxa(v=vs.85)) для получения определения класса.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    В следующем примере показано, как запросить определение класса.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

Определение класса в C++ можно получить, указав только имя класса и путь к конкретному экземпляру. В следующей процедуре описывается извлечение определения класса в C++.

**Извлечение определения класса в C++**

-   Выполните вызов функций [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    В следующем примере показано, как вызвать функцию [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    В предыдущем примере кода \# для правильной компиляции требуется следующая инструкция include.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
