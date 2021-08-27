---
description: библиотеку типов сценариев wmi можно использовать для вызова методов API-сценариев wmi из Microsoft Visual Studio и в файлах сценариев Windows.
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
ms.openlocfilehash: 20e5a2aa10bccfbd91b003f1db120691b6c61bb4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881174"
---
# <a name="using-the-wmi-scripting-type-library"></a>Использование библиотеки типов сценариев WMI

библиотеку типов сценариев wmi можно использовать для вызова методов API-сценариев wmi из Microsoft Visual Studio и в файлах сценариев Windows.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Использование библиотеки типов сценариев WMI с Microsoft Visual Studio

> [!Note]  
> компоненты Visual InterDev 6,0 интегрированы в [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).

 

В следующей процедуре описывается, как включить в интегрированной среде разработки (IDE) сведения о библиотеке типов Вбемскриптинг.

**Добавление библиотеки типов сценариев WMI в ссылки проекта**

1.  в меню **Project** выберите команду **добавить ссылки** .
2.  На вкладке COM в поле **Добавить ссылку** выберите БИБЛИОТЕКУ Microsoft WMI Scripting v 1.2.
3.  Если в списке ссылки нет соответствующего параметра, добавьте его с помощью **кнопки Обзор** в поле **ссылки** . На странице **Обзор** открывается поле **Добавить ссылку** , позволяющее найти библиотеку типов вбемскриптинг.

    Библиотека типов Вбемскриптинг находится в файле Wbemdisp. tlb в каталоге% WINDIR% \\ system32 \\ WBEM.

4.  Выберите файл и нажмите **Открыть**. Библиотека Microsoft WMI Scripting V 1.2 отображается в списке ссылок. Убедитесь, что в списке рядом с этим элементом выбрано поле.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>использование библиотеки типов сценариев WMI с Windows сервера сценариев 2,0

ссылку на **вбемскриптинг. SWbemLocator** можно включить в файл WSF-файла сценария Windows, в отличие от скрипта, написанного на Visual Basic, scripting Edition или других языках сценариев. Это позволяет использовать вместо значений константные имена. Например, при настройке проверки подлинности используйте **вбемаусентикатионлевелпктприваци** вместо значения 6.

Сценарии могут подключаться с помощью API скриптов для библиотеки типов WMI, используя следующие методы:

-   Указание идентификатора GUID Вбемскриптинг в методах VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) и [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    это оповещение Windows сервере сценариев для подключения к набору объектов WMI.

    В следующем примере кода VBScript создается новый объект [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Использование [строки моникера](constructing-a-moniker-string.md) "винмгмтс:" при получении нового или существующего объекта.

    В следующем примере кода VBScript используется моникер "винмгмтс:" для получения экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) со свойством **Handle** , равным 0 (ноль). **Handle** — это ключевое свойство для этого класса.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Ссылка на библиотеку типов WMI с помощью &lt; тега Reference в &gt; формате XML-файла WSH 2,0. Если используется &lt; &gt; тег Reference, тег должен иметь либо атрибут **UUID** , значение которого является **идентификатором GUID** библиотеки типов WMI, либо (рекомендуется) атрибут объекта, значение которого является **ИДЕНТИФИКАТОРом ProgID** любого из объектов сценариев WMI, которые можно создать.

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

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API сценариев для инструментария WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
