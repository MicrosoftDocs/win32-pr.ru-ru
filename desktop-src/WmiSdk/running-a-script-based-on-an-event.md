---
description: Стандартный потребитель, реализованный классом Активескриптевентконсумер, позволяет компьютеру выполнять сценарий и предпринимать действия при возникновении важных событий, чтобы гарантировать, что компьютер сможет автоматически обнаруживать и устранять неполадки.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Выполнение скрипта на основе события
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b5950ae8a4e7260932fd4df559a73f3abea2bfaf7722444db0b92470649dd312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816742"
---
# <a name="running-a-script-based-on-an-event"></a>Выполнение скрипта на основе события

Стандартный потребитель, реализованный классом [**активескриптевентконсумер**](activescripteventconsumer.md) , позволяет компьютеру выполнять сценарий и предпринимать действия при возникновении важных событий, чтобы гарантировать, что компьютер сможет автоматически обнаруживать и устранять неполадки.

Этот потребитель загружается по умолчанию в пространстве имен **корневой \\ подписки** .

Можно настроить производительность всех экземпляров [**активескриптевентконсумер**](activescripteventconsumer.md) в системе, задав значения свойства **timeout** или **Максимумскриптс** в одном экземпляре [**скриптингстандардконсумерсеттинг**](scriptingstandardconsumersetting.md).

Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md). Следующая процедура, которая добавляет к базовой процедуре, относится к классу [**активескриптевентконсумер**](activescripteventconsumer.md) и описывает создание объекта-получателя события, запускающего скрипт.

> [!Caution]  
> Класс [**активескриптевентконсумер**](activescripteventconsumer.md) имеет специальные ограничения безопасности. Этот стандартный потребитель должен быть настроен локальным членом группы "Администраторы" на локальном компьютере. Если для создания подписки используется учетная запись домена, учетная запись LocalSystem должна иметь необходимые разрешения в домене, чтобы убедиться, что создатель является членом локальной группы администраторов.

 

В следующей процедуре описывается создание объекта-получателя события, выполняющего скрипт.

**Создание объекта-получателя события, выполняющего Скрипт**

1.  Напишите скрипт для запуска при возникновении события.

    Скрипт можно написать на любом языке, но убедитесь, что на вашем компьютере установлен обработчик скриптов для выбранного языка. Сценарий не должен использовать объекты скриптов WMI.

    Только администратор может настроить потребителя сценариев, и сценарий выполняется под учетными данными LocalSystem, что дает потребителю широкие возможности, за исключением доступа к сети. Однако сценарий не имеет доступа к конкретным данным входа пользователя, например к переменным среды и сетевым папкам.

2.  В файле MOF-файл (MOF) создайте экземпляр [**активескриптевентконсумер**](activescripteventconsumer.md) для получения событий, которые вы запрашиваете в запросе.

    Текст скрипта можно разместить в **скрипттекст** или указать путь и имя файла скрипта в **скриптфиленаме**. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).

3.  Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md), присвойте ему имя, а затем создайте запрос для указания типа события, который активирует выполнение скрипта.

    Дополнительные сведения см. в разделе [запросы с помощью WQL](querying-with-wql.md).

4.  Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**активескриптевентконсумер**](activescripteventconsumer.md).
5.  Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).

В примерах, приведенных в следующем разделе, показаны два способа реализации скрипта, управляемого событиями. В первом примере используется скрипт, определенный во внешнем файле, а во втором примере используется скрипт, встроенный в MOF-код. Примеры находятся в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).

## <a name="example-using-an-external-script"></a>Пример использования внешнего скрипта

В следующей процедуре описывается использование примера внешнего скрипта.

**Использование примера внешнего скрипта**

1.  Создайте файл с именем c: \\Asec.vbs, а затем скопируйте в него сценарий из этого примера.
2.  Скопируйте список MOF в текстовый файл и сохраните его с расширением. mof.
3.  В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.

    **Mofcomp** *filename * * *. mof**

4.  Запустите калькулятор, который создает процесс calc.exe. Подождите более пяти секунд, закройте окно калькулятора, а затем найдите в каталоге C: \\ файл с именем АСЕК. log.

    Следующий текст похож на текст, который будет содержаться в файле АСЕК. log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

В следующем примере кода VBScript показан скрипт, который вызывается, когда постоянный потребитель получает событие. Объект **таржетевент** является экземпляром [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md) , поэтому он имеет свойство с именем **TargetInstance**, которое является экземпляром [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , используемым для срабатывания события. Класс **\_ процесса Win32** имеет свойства **усермодетиме** и **кернелмодетиме** , которые помещаются в файл журнала, созданный сценарием.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



Следующий пример кода MOF вызывает скрипт при получении события. Он создает фильтр, потребитель и привязку между ними в пространстве имен **корневой \\ подписки** .

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Пример с использованием встроенного скрипта

В следующей процедуре описывается использование встроенного примера скрипта.

**Использование примера встроенного скрипта**

1.  Скопируйте список MOF в этом разделе в текстовый файл и сохраните его с расширением. mof.
2.  В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.

    **Mofcomp** *filename * * *. mof**

В следующем примере кода MOF создается фильтр, потребитель и привязка между ними, а также включается встроенный скрипт.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Мониторинг событий и реагирование на них с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
