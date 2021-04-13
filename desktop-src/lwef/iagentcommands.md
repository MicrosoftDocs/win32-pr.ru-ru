---
title: иаженткоммандс
description: иаженткоммандс
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533149"
---
# <a name="iagentcommands"></a>иаженткоммандс

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Сервер Microsoft Agent поддерживает список команд, доступных пользователю в данный момент. В этот список входят команды, определяемые сервером для общего взаимодействия, такие как свойства Hide и Microsoft Agent, список доступных (но не являющихся входных) клиентов, а также команды, определенные текущим активным клиентом. Первые два набора команд являются глобальными командами. Это значит, что они доступны в любое время, независимо от клиента ввода-активности. Определяемые клиентом команды доступны только в том случае, если этот клиент является входным.

Получите интерфейс **иаженткоммандс** , выполнив запрос к интерфейсу [**иажентчарактер**](https://www.bing.com/search?q=**IAgentCharacter**) для **иаженткоммандс**. Каждое клиентское приложение Microsoft Agent может определять коллекцию команд, называемых коллекцией [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Чтобы добавить [**команду**](/windows/desktop/lwef/the-command-object) в коллекцию, используйте метод [**Add**](add-method.md) или [**INSERT**](insert-method.md) . Несмотря на то, что свойства **команды** можно указать с помощью методов [**иаженткомманд**](iagentcommand.md) , для оптимальной производительности кода укажите все свойства **команды** в методах [**иаженткоммандс:: Add**](iagentcommands--add.md) или [**иаженткоммандс:: INSERT**](iagentcommands--insert.md) при первоначальной установке свойств для новой **команды**. Для запроса или изменения параметров свойств можно использовать методы **иаженткомманд** .

Для каждой [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) можно определить, отображается ли команда во всплывающем меню символа, в окне "голоса" в обоих случаях или в любом из них. Например, если вы хотите, чтобы команда отображалась во всплывающем меню для символа, задайте [**заголовок**](caption-property.md) и [**видимые**](visible-property.md) свойства команды. Чтобы отобразить команду в окне " **речь**", задайте свойства **Caption** и [**Voice**](voice-property.md) команды.

Пользователь может получить доступ к отдельным командам в коллекции Commands, только если клиентское приложение имеет входные данные и этот символ является видимым. Поэтому, как правило, необходимо задать свойства [**Caption**](caption-property.md), [**воицекаптион**](voicecaption-property.md)и [**Voice**](voice-property.md) для объекта коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , а также для команд в коллекции, так как это помещает запись для коллекции **команд** во всплывающем меню символа и в окне "Voice Commands". Когда пользователь переключается на клиент, выбрав запись **команды** , сервер автоматически делает ввод клиента активным, уведомляя клиентское приложение с помощью [**Иажентнотифисинк:: активатеинпутстате**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) и делает доступными **команды** в коллекции. Сервер также уведомляет клиента, что он больше не является входным, с событием **иажентнотифисинк:: активатеинпутстате** . Это позволяет серверу предоставлять и принимать только **команды** , которые применяются к текущему контексту ввода-активного клиента. Это также позволяет избежать конфликтов имен [**команд**](/windows/desktop/lwef/the-command-object)между клиентами.

Клиент также может явным образом запросить у клиента ввода-активности клиент, используя метод [**иажентчарактер:: Activate**](iagentcharacter--activate.md) . Этот метод также поддерживает настройку приложения так, чтобы он не был клиентом input-Active. Этот метод можно использовать при совместном использовании символа с другим приложением, настроив приложение в качестве входных данных, если окно приложения получает фокус и не является активным при потере фокуса.

Аналогичным образом можно использовать [**иажентчарактер:: Activate**](iagentcharacter--activate.md) , чтобы настроить приложение в качестве активного клиента символа. Активный клиент — это клиент, который получает входные данные, когда его символ является самым верхним. При изменении этого состояния сервер уведомляет ваше приложение с событием [**иажентнотифисинкекс:: активеклиентчанже**](iagentnotifysinkex--activeclientchange.md) .

При отображении всплывающего меню символа изменения свойств коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) или команд в его коллекции не отображаются, пока пользователь не отобразит меню. Однако при открытии в окне "Voice Commands" отображаются изменения по мере их возникновения.

**Иаженткоммандс** определяет интерфейс, позволяющий приложениям добавлять, удалять, задавать и запрашивать свойства для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Эти функции также доступны из [**иаженткоммандсекс**](iagentcommandsex.md).

Коллекция [**Commands**](/windows/desktop/lwef/the-commands-collection-object) может отображаться как команда во всплывающем меню, так и в окне "речь" для символа. Чтобы отобразить коллекцию **команд** , необходимо задать свойство [**Caption**](caption-property.md) . В следующей таблице показано, как свойства коллекции **Commands** влияют на ее представление.



| Свойство Caption | Voice-Caption, свойство | Свойство Voice | Свойство Visible | Отображается во всплывающем меню "символ"             | Отображается в окне "Voice Commands"                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Да              | Да                    | Да            | True             | Да, с использованием [ **заголовка**](caption-property.md) | Да, с помощью [ **воицекаптион**](voicecaption-property.md) |
| Да              | Да                    | Без ¹            | True             | Да, с использованием [ **заголовка**](caption-property.md) | Нет                                                       |
| Да              | Да                    | Да            | False            | нет                                             | Да, с помощью [ **воицекаптион**](voicecaption-property.md) |
| Да              | Да                    | Без ¹            | False            | нет                                             | Нет                                                       |
| Без ¹              | Да                    | Да            | True             | нет                                             | Да, с помощью [ **воицекаптион**](voicecaption-property.md) |
| Без ¹              | Да                    | Да            | False            | нет                                             | Да, с помощью [ **воицекаптион**](voicecaption-property.md) |
| Без ¹              | Да                    | Без ¹            | True             | нет                                             | Нет                                                       |
| Без ¹              | Да                    | Без ¹            | False            | нет                                             | Нет                                                       |
| Да              | Без ¹                    | Да            | True             | Да, с использованием [ **заголовка**](caption-property.md) | Да, с использованием [ **заголовка**](caption-property.md)           |
| Да              | Без ¹                    | Без ¹            | True             | Да                                            | Нет                                                       |
| Да              | Без ¹                    | Да            | False            | нет                                             | Да, с использованием [ **заголовка**](caption-property.md)           |
| Да              | Без ¹                    | Без ¹            | False            | нет                                             | Нет                                                       |
| Без ¹              | Без ¹                    | Да            | True             | нет                                             | Без ²                                                      |
| Без ¹              | Без ¹                    | Да            | False            | нет                                             | Без ²                                                      |
| Без ¹              | Без ¹                    | Без ¹            | True             | нет                                             | Нет                                                       |
| Без ¹              | Без ¹                    | Без ¹            | False            | нет                                             | Нет                                                       |



 

¹, если значение свойства равно null. В некоторых языках программирования пустая строка не может интерпретироваться как строка со значением NULL.

² команда по-прежнему доступна для передачи голоса.

**Методы в порядке таблицы Vtable**



| Методы Иаженткоммандс                           | Описание                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Извлекает объект [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .              |
| [**GetCount**](iagentcommands--getcount.md)     | Возвращает значение количества [**команд**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) . |
| [**сеткаптион**](iagentcommands--setcaption.md) | Задает значение свойства [**Caption**](caption-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**Субтитр**](iagentcommands--getcaption.md) | Возвращает значение свойства [**Caption**](caption-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**сетвоице**](iagentcommands--setvoice.md)     | Задает значение свойства [**Voice**](voice-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .        |
| [**Voice**](iagentcommands--getvoice.md)     | Возвращает значение свойства [**Voice**](voice-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .      |
| [**сетвисибле**](iagentcommands--setvisible.md) | Задает значение свойства [**Visible**](visible-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**Во всех видимых**](iagentcommands--getvisible.md) | Возвращает значение свойства [**Visible**](visible-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Добавить**](iagentcommands--add.md)               | Добавляет объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекцию [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                       |
| [**Вставляет**](iagentcommands--insert.md)         | Вставляет объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекцию [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**Отменит**](iagentcommands--remove.md)         | Удаляет объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Удаляет все [**Командные**](/windows/desktop/lwef/the-command-object) объекты из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .               |



 

 

 