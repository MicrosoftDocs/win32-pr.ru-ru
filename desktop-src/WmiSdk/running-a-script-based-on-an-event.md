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
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912751"
---
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="4adee-103">Выполнение скрипта на основе события</span><span class="sxs-lookup"><span data-stu-id="4adee-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="4adee-104">Стандартный потребитель, реализованный классом [**активескриптевентконсумер**](activescripteventconsumer.md) , позволяет компьютеру выполнять сценарий и предпринимать действия при возникновении важных событий, чтобы гарантировать, что компьютер сможет автоматически обнаруживать и устранять неполадки.</span><span class="sxs-lookup"><span data-stu-id="4adee-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="4adee-105">Этот потребитель загружается по умолчанию в пространстве имен **корневой \\ подписки** .</span><span class="sxs-lookup"><span data-stu-id="4adee-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="4adee-106">Можно настроить производительность всех экземпляров [**активескриптевентконсумер**](activescripteventconsumer.md) в системе, задав значения свойства **timeout** или **Максимумскриптс** в одном экземпляре [**скриптингстандардконсумерсеттинг**](scriptingstandardconsumersetting.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="4adee-107">Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="4adee-108">Следующая процедура, которая добавляет к базовой процедуре, относится к классу [**активескриптевентконсумер**](activescripteventconsumer.md) и описывает создание объекта-получателя события, запускающего скрипт.</span><span class="sxs-lookup"><span data-stu-id="4adee-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="4adee-109">Класс [**активескриптевентконсумер**](activescripteventconsumer.md) имеет специальные ограничения безопасности.</span><span class="sxs-lookup"><span data-stu-id="4adee-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="4adee-110">Этот стандартный потребитель должен быть настроен локальным членом группы "Администраторы" на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4adee-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="4adee-111">Если для создания подписки используется учетная запись домена, учетная запись LocalSystem должна иметь необходимые разрешения в домене, чтобы убедиться, что создатель является членом локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="4adee-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="4adee-112">В следующей процедуре описывается создание объекта-получателя события, выполняющего скрипт.</span><span class="sxs-lookup"><span data-stu-id="4adee-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="4adee-113">**Создание объекта-получателя события, выполняющего Скрипт**</span><span class="sxs-lookup"><span data-stu-id="4adee-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="4adee-114">Напишите скрипт для запуска при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="4adee-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="4adee-115">Скрипт можно написать на любом языке, но убедитесь, что на вашем компьютере установлен обработчик скриптов для выбранного языка.</span><span class="sxs-lookup"><span data-stu-id="4adee-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="4adee-116">Сценарий не должен использовать объекты скриптов WMI.</span><span class="sxs-lookup"><span data-stu-id="4adee-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="4adee-117">Только администратор может настроить потребителя сценариев, и сценарий выполняется под учетными данными LocalSystem, что дает потребителю широкие возможности, за исключением доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="4adee-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="4adee-118">Однако сценарий не имеет доступа к конкретным данным входа пользователя, например к переменным среды и сетевым папкам.</span><span class="sxs-lookup"><span data-stu-id="4adee-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="4adee-119">В файле MOF-файл (MOF) создайте экземпляр [**активескриптевентконсумер**](activescripteventconsumer.md) для получения событий, которые вы запрашиваете в запросе.</span><span class="sxs-lookup"><span data-stu-id="4adee-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="4adee-120">Текст скрипта можно разместить в **скрипттекст** или указать путь и имя файла скрипта в **скриптфиленаме**.</span><span class="sxs-lookup"><span data-stu-id="4adee-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="4adee-121">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="4adee-122">Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md), присвойте ему имя, а затем создайте запрос для указания типа события, который активирует выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="4adee-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="4adee-123">Дополнительные сведения см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="4adee-124">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**активескриптевентконсумер**](activescripteventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="4adee-125">Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="4adee-126">В примерах, приведенных в следующем разделе, показаны два способа реализации скрипта, управляемого событиями.</span><span class="sxs-lookup"><span data-stu-id="4adee-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="4adee-127">В первом примере используется скрипт, определенный во внешнем файле, а во втором примере используется скрипт, встроенный в MOF-код.</span><span class="sxs-lookup"><span data-stu-id="4adee-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="4adee-128">Примеры находятся в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4adee-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="4adee-129">Пример использования внешнего скрипта</span><span class="sxs-lookup"><span data-stu-id="4adee-129">Example Using an External Script</span></span>

<span data-ttu-id="4adee-130">В следующей процедуре описывается использование примера внешнего скрипта.</span><span class="sxs-lookup"><span data-stu-id="4adee-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="4adee-131">**Использование примера внешнего скрипта**</span><span class="sxs-lookup"><span data-stu-id="4adee-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="4adee-132">Создайте файл с именем c: \\Asec.vbs, а затем скопируйте в него сценарий из этого примера.</span><span class="sxs-lookup"><span data-stu-id="4adee-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="4adee-133">Скопируйте список MOF в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="4adee-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="4adee-134">В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="4adee-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="4adee-135">**Mofcomp** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="4adee-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="4adee-136">Запустите калькулятор, который создает процесс calc.exe.</span><span class="sxs-lookup"><span data-stu-id="4adee-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="4adee-137">Подождите более пяти секунд, закройте окно калькулятора, а затем найдите в каталоге C: \\ файл с именем АСЕК. log.</span><span class="sxs-lookup"><span data-stu-id="4adee-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="4adee-138">Следующий текст похож на текст, который будет содержаться в файле АСЕК. log.</span><span class="sxs-lookup"><span data-stu-id="4adee-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="4adee-139">В следующем примере кода VBScript показан скрипт, который вызывается, когда постоянный потребитель получает событие.</span><span class="sxs-lookup"><span data-stu-id="4adee-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="4adee-140">Объект **таржетевент** является экземпляром [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md) , поэтому он имеет свойство с именем **TargetInstance**, которое является экземпляром [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , используемым для срабатывания события.</span><span class="sxs-lookup"><span data-stu-id="4adee-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="4adee-141">Класс **\_ процесса Win32** имеет свойства **усермодетиме** и **кернелмодетиме** , которые помещаются в файл журнала, созданный сценарием.</span><span class="sxs-lookup"><span data-stu-id="4adee-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


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



<span data-ttu-id="4adee-142">Следующий пример кода MOF вызывает скрипт при получении события.</span><span class="sxs-lookup"><span data-stu-id="4adee-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="4adee-143">Он создает фильтр, потребитель и привязку между ними в пространстве имен **корневой \\ подписки** .</span><span class="sxs-lookup"><span data-stu-id="4adee-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

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

## <a name="example-using-inline-script"></a><span data-ttu-id="4adee-144">Пример с использованием встроенного скрипта</span><span class="sxs-lookup"><span data-stu-id="4adee-144">Example Using Inline Script</span></span>

<span data-ttu-id="4adee-145">В следующей процедуре описывается использование встроенного примера скрипта.</span><span class="sxs-lookup"><span data-stu-id="4adee-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="4adee-146">**Использование примера встроенного скрипта**</span><span class="sxs-lookup"><span data-stu-id="4adee-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="4adee-147">Скопируйте список MOF в этом разделе в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="4adee-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="4adee-148">В окне командной строки Скомпилируйте MOF-файл с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="4adee-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="4adee-149">**Mofcomp** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="4adee-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="4adee-150">В следующем примере кода MOF создается фильтр, потребитель и привязка между ними, а также включается встроенный скрипт.</span><span class="sxs-lookup"><span data-stu-id="4adee-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4adee-151">См. также</span><span class="sxs-lookup"><span data-stu-id="4adee-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adee-152">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="4adee-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
