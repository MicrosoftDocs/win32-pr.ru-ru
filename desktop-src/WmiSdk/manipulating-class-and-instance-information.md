---
description: Инструментарий WMI предоставляет разнообразные методы для получения и управления сведениями о классе и экземпляре WMI, использовании Microsoft PowerShell, Visual&\# 160; Basic Scripting Edition (VBScript) и C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Управление сведениями о классе и экземпляре
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712771"
---
# <a name="manipulating-class-and-instance-information"></a>Управление сведениями о классе и экземпляре

Инструментарий WMI предоставляет разнообразные методы для получения и управления сведениями о классе и экземпляре WMI, использовании Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) и C++.

В следующей таблице перечислены разделы, в которых обсуждаются методы извлечения и управления сведениями о классе и экземпляре WMI.



| Раздел                                                                                  | Описание                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md)         | Получение и установка данных из и в репозиторий данных WMI.                                                                                                                 |
| [Изменение свойства экземпляра](modifying-an-instance-property.md)                   | Измените сведения в экземпляре после получения.                                                                                                                     |
| [Изменение наследования экземпляра](changing-the-inheritance-of-an-instance.md) | Измените родительский класс экземпляра.                                                                                                                                           |
| [Изменение метода](modifying-a-method.md)                                           | Измените параметры экземпляра.                                                                                                                                             |
| [Перечисление WMI](enumerating-wmi.md)                                                 | Перечисление объектов WMI.                                                                                                                                                            |
| [Запрос WMI](querying-wmi.md)                                                       | Запрос объектов WMI.                                                                                                                                                                |
| [Вызов метода](calling-a-method.md)                                               | Используйте связанные методы, созданные корпорацией Майкрософт или другими сторонними разработчиками для дальнейшего управления объектами WMI, или, в противном случае, напрямую влияют на объект, который представляет объект WMI. |
| [Доступ к коллекции](accessing-a-collection.md)                                   | Перечисление коллекций в скрипте.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Обработка данных с помощью VBScript

Можно использовать прямой доступ для доступа к свойствам WMI класса или экземпляра WMI непосредственно в [**SWbemObject**](swbemobject.md), а не через [коллекцию](accessing-a-collection.md) свойств этого объекта. Можно также выполнить методы для этого объекта в собственном стиле языка программирования, а не использовать вызов [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) . Например, метод [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) в [**\_ процессе Win32**](/windows/desktop/CIMWin32Prov/win32-process) содержал три параметра в Windows 2000, но имеет четыре параметра в Windows Server 2003.

С помощью прямого доступа можно рассматривать свойства и методы WMI, как если бы они были свойствами автоматизации и методами [**SWbemObject**](swbemobject.md).

В следующем примере показано, как можно получить доступ к свойству.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



В следующем примере показано, как можно получить доступ к свойству при наличии прямого доступа.


```VB
VolumeName = MyDisk.VolumeName
```



Цепочки объектов также являются приемлемыми.

В следующем примере показано, как получить доступ к свойству объекта, внедренного в другой объект.


```VB
value = MyComputer.MyDisk.VolumeName
```



В следующем примере показано, как получить доступ к свойству с помощью нотации индекса массива.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



В следующем примере кода VBScript показано, как создать экземпляр входных параметров в методе [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) в классе [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) в качестве [**SWbemObject**](swbemobject.md), заполнить входные свойства, а затем выполнить метод **CREATE** с помощью [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md).

Свойство [**SWbemObject. Methods \_**](swbemobject-methods-.md) Возвращает коллекцию [**свбеммесодсет**](swbemmethodset.md) методов [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) . Членами набора методов являются объекты [**свбеммесод**](swbemmethod.md) и [**свбеммесод. outs**](swbemmethod-inparameters.md) Возвращает входные параметры для метода [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Требуемый входной параметр *командной строки* имеет значение "calc.exe". Затем метод выполняется [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md), что приводит к запуску calc.exe процесса.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



В следующем примере кода показано, как выполнить предыдущую операцию с помощью прямого доступа.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Дополнительные сведения см. в разделе [вызов метода поставщика](calling-a-provider-method.md) и [Создание скриптов с помощью SWbemObject](scripting-with-swbemobject.md).

 

 
