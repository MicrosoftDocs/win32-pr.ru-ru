---
description: Библиотеку типов сценариев WMI можно использовать для вызова методов API сценариев WMI из Microsoft Visual Studio и в файлах Windows Script, WSF-файлов.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Использование библиотеки типов сценариев WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702652"
---
# <a name="using-the-wmi-scripting-type-library"></a>Использование библиотеки типов сценариев WMI

Библиотеку типов сценариев WMI можно использовать для вызова методов API сценариев WMI из Microsoft Visual Studio и в файлах Windows Script, WSF-файлов.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Использование библиотеки типов сценариев WMI с Microsoft Visual Studio

> [!Note]  
> Компоненты Visual InterDev 6,0 интегрированы в [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).

 

В следующей процедуре описывается, как включить в интегрированной среде разработки (IDE) сведения о библиотеке типов Вбемскриптинг.

**Добавление библиотеки типов сценариев WMI в ссылки проекта**

1.  В меню **проект** выберите команду **Добавить ссылки** .
2.  На вкладке COM в поле **Добавить ссылку** выберите БИБЛИОТЕКУ Microsoft WMI Scripting v 1.2.
3.  Если в списке ссылки нет соответствующего параметра, добавьте его с помощью **кнопки Обзор** в поле **ссылки** . На странице **Обзор** открывается поле **Добавить ссылку** , позволяющее найти библиотеку типов вбемскриптинг.

    Библиотека типов Вбемскриптинг находится в файле Wbemdisp. tlb в каталоге% WINDIR% \\ system32 \\ WBEM.

4.  Выберите файл и нажмите **Открыть**. Библиотека Microsoft WMI Scripting V 1.2 отображается в списке ссылок. Убедитесь, что в списке рядом с этим элементом выбрано поле.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Использование библиотеки типов сценариев WMI с сервером сценариев Windows 2,0

Можно включить ссылку на **вбемскриптинг. SWbemLocator** в файл WSF сервера сценариев Windows, в отличие от скрипта, написанного на Visual Basic, Scripting Edition или других языках сценариев. Это позволяет использовать вместо значений константные имена. Например, при настройке проверки подлинности используйте **вбемаусентикатионлевелпктприваци** вместо значения 6.

Сценарии могут подключаться с помощью API скриптов для библиотеки типов WMI, используя следующие методы:

-   Указание идентификатора GUID Вбемскриптинг в методах VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) и [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    Это оповещает сервер сценариев Windows о подключении к набору объектов WMI.

    В следующем примере кода VBScript создается новый объект [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Использование [строки моникера](constructing-a-moniker-string.md) "винмгмтс:" при получении нового или существующего объекта.

    В следующем примере кода VBScript используется моникер "винмгмтс:" для получения экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) со свойством **Handle** , равным 0 (ноль). **Handle** — это ключевое свойство для этого класса.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Ссылка на библиотеку типов WMI с помощью <reference> тега формата XML-файла WSH 2,0. При использовании <reference> тега тег должен иметь либо атрибут **UUID** , значение которого является **идентификатором GUID** библиотеки типов WMI, либо (рекомендуется) атрибут объекта, значение которого является **идентификатором ProgID** любого из объектов сценариев WMI, которые можно создать.

    В следующем примере кода VBScript используется идентификатор PROGID "Вбемскриптинг". Чтобы выполнить сценарий, сохраните текст в файл с расширением. wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Использование <**объекта**> тега для создания объекта скрипта WMI. Можно указать атрибут **ID** со значением имени, которое ссылается на создаваемый объект скрипта WMI, и атрибут **ProgID** , равный проид объекта сценариев WMI.

    Следующий сценарий WSH отображает имя узла и количество процессоров на локальном компьютере. Чтобы выполнить сценарий, сохраните текст в файл с расширением. wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API сценариев для инструментария WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
