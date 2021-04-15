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
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Запуск программы из командной строки на основе события

Класс [**коммандлинивентконсумер**](commandlineeventconsumer.md) запускает указанную исполняемую программу из командной строки при возникновении указанного события. Этот класс является стандартным потребителем событий, предоставляемым инструментарием WMI.

При использовании [**коммандлинивентконсумер**](commandlineeventconsumer.md)необходимо защитить исполняемый файл, который требуется запустить. Если исполняемый файл не находится в безопасном месте или не защищен с помощью строгого списка управления доступом (ACL), пользователь без прав доступа может заменить исполняемый файл другим исполняемым файлом. Классы [**Win32 \_ Логикалфилесекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) или [**Win32 \_ логикалшаресекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) можно использовать для изменения программными средствами безопасности файла или общей папки. Дополнительные сведения см. [в разделе Создание дескриптора безопасности для нового объекта в C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

Базовая процедура использования стандартных потребителей всегда одинакова и находится в [мониторинге и реагировании на события со стандартными потребителями](monitoring-and-responding-to-events-with-standard-consumers.md). Следующая процедура добавляет в основную процедуру, относящуюся к классу [**коммандлинивентконсумер**](commandlineeventconsumer.md) , и описывает создание объекта-получателя события, запускающего программу.

> [!Caution]
>
> Класс [**коммандлинивентконсумер**](commandlineeventconsumer.md) имеет специальные ограничения безопасности. Этот стандартный потребитель должен быть настроен локальным членом группы "Администраторы" на локальном компьютере. Если для создания подписки используется учетная запись домена, учетная запись LocalSystem должна иметь необходимые разрешения в домене, чтобы убедиться, что создатель является членом локальной группы администраторов.
>
> [**Коммандлинивентконсумер**](commandlineeventconsumer.md) нельзя использовать для запуска процесса, выполняемого в интерактивном режиме.

 

В следующей процедуре описывается создание объекта-получателя события, запускающего процесс из командной строки.

**Создание объекта-получателя события, запускающего процесс из командной строки**

1.  В файле MOF-файл (MOF) создайте экземпляр [**коммандлинивентконсумер**](commandlineeventconsumer.md) для получения событий, которые вы запрашиваете в запросе. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).
2.  Создайте экземпляр [**\_ \_ EventFilter**](--eventfilter.md) и присвойте ему имя.
3.  Создайте запрос для указания типа события. Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).
4.  Создайте экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать фильтр с экземпляром [**коммандлинивентконсумер**](commandlineeventconsumer.md).
5.  Скомпилируйте MOF-файл с помощью [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Пример

В следующем примере кода создается новый класс с именем "Микмдлинеконсумер" для создания событий при создании экземпляра нового класса в конце MOF-файла. Этот пример находится в MOF-коде, но экземпляры можно создавать программно с помощью [API скриптов для WMI](scripting-api-for-wmi.md) или [COM API для WMI](com-api-for-wmi.md).

В следующей процедуре описывается создание нового класса с именем Микмдлинеконсумер.

**Создание нового класса с именем Микмдлинеконсумер**

1.  Создайте файл c: \\ cmdline \_test.bat с командой, выполняющей видимую программу, например "calc.exe".
2.  Скопируйте MOF в текстовый файл и сохраните его с расширением. mof.
3.  В командное окно Скомпилируйте MOF-файл с помощью следующей команды: **mofcomp filename. mof**.

> [!Note]  
> Программа, указанная в поле cmdline \_test.bat, должна выполняться.

 

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мониторинг событий и реагирование на них с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
