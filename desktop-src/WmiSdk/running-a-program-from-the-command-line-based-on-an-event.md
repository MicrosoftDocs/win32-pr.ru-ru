---
description: Класс Коммандлинивентконсумер запускает указанную исполняемую программу из командной строки при возникновении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Запуск программы из командной строки на основе события
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701996"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="7714b-104">Запуск программы из командной строки на основе события</span><span class="sxs-lookup"><span data-stu-id="7714b-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="7714b-105">Класс [**коммандлинивентконсумер**](commandlineeventconsumer.md) запускает указанную исполняемую программу из командной строки при возникновении указанного события.</span><span class="sxs-lookup"><span data-stu-id="7714b-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="7714b-106">Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7714b-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="7714b-107">При использовании [**коммандлинивентконсумер**](commandlineeventconsumer.md)необходимо защитить исполняемый файл, который требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="7714b-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="7714b-108">Если исполняемый файл не находится в безопасном месте или не защищен с помощью строгого списка управления доступом (ACL), пользователь без прав доступа может заменить исполняемый файл другим исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="7714b-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="7714b-109">Классы [**Win32 \_ Логикалфилесекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) или [**Win32 \_ логикалшаресекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) можно использовать для изменения программными средствами безопасности файла или общей папки.</span><span class="sxs-lookup"><span data-stu-id="7714b-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="7714b-110">Дополнительные сведения см. [в разделе Создание дескриптора безопасности для нового объекта в C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="7714b-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="7714b-111">Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="7714b-112">Следующая процедура добавляет в основную процедуру, относящуюся к классу [**коммандлинивентконсумер**](commandlineeventconsumer.md) , и описывает создание объекта-получателя события, запускающего программу.</span><span class="sxs-lookup"><span data-stu-id="7714b-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="7714b-113">Класс [**коммандлинивентконсумер**](commandlineeventconsumer.md) имеет специальные ограничения безопасности.</span><span class="sxs-lookup"><span data-stu-id="7714b-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="7714b-114">Этот стандартный потребитель должен быть настроен локальным членом группы "Администраторы" на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7714b-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="7714b-115">Если для создания подписки используется учетная запись домена, учетная запись LocalSystem должна иметь необходимые разрешения в домене, чтобы убедиться, что создатель является членом локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="7714b-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="7714b-116">[**Коммандлинивентконсумер**](commandlineeventconsumer.md) нельзя использовать для запуска процесса, выполняемого в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="7714b-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="7714b-117">В следующей процедуре описывается создание объекта-получателя события, запускающего процесс из командной строки.</span><span class="sxs-lookup"><span data-stu-id="7714b-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="7714b-118">**Создание объекта-получателя события, запускающего процесс из командной строки**</span><span class="sxs-lookup"><span data-stu-id="7714b-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="7714b-119">В файле MOF-файл (MOF) создайте экземпляр [**коммандлинивентконсумер**](commandlineeventconsumer.md) для получения событий, которые вы запрашиваете в запросе.</span><span class="sxs-lookup"><span data-stu-id="7714b-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="7714b-120">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="7714b-121">Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и присвойте ему имя.</span><span class="sxs-lookup"><span data-stu-id="7714b-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="7714b-122">Создайте запрос для указания типа события.</span><span class="sxs-lookup"><span data-stu-id="7714b-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="7714b-123">Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="7714b-124">Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**коммандлинивентконсумер**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="7714b-125">Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="7714b-126">Пример</span><span class="sxs-lookup"><span data-stu-id="7714b-126">Example</span></span>

<span data-ttu-id="7714b-127">В следующем примере кода создается новый класс с именем "Микмдлинеконсумер" для создания событий при создании экземпляра нового класса в конце MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="7714b-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="7714b-128">Этот пример находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7714b-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="7714b-129">В следующей процедуре описывается создание нового класса с именем Микмдлинеконсумер.</span><span class="sxs-lookup"><span data-stu-id="7714b-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="7714b-130">**Создание нового класса с именем Микмдлинеконсумер**</span><span class="sxs-lookup"><span data-stu-id="7714b-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="7714b-131">Создайте файл c: \\ cmdline \_test.bat с командой, выполняющей видимую программу, например "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="7714b-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="7714b-132">Скопируйте MOF в текстовый файл и сохраните его с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="7714b-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="7714b-133">В командное окно Скомпилируйте MOF-файл с помощью следующей команды: **mofcomp filename. mof**.</span><span class="sxs-lookup"><span data-stu-id="7714b-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="7714b-134">Программа, указанная в поле cmdline \_test.bat, должна выполняться.</span><span class="sxs-lookup"><span data-stu-id="7714b-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a><span data-ttu-id="7714b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="7714b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7714b-136">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="7714b-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
