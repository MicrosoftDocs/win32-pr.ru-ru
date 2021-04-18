---
title: иаженткомманд
description: иаженткомманд
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691498"
---
# <a name="iagentcommand"></a>иаженткомманд

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**Command**](/windows/desktop/lwef/the-command-object) — это элемент в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Сервер предоставляет пользователю доступ к командам, которые клиентское приложение получает активным. Чтобы получить **команду**, вызовите [**иаженткоммандс::-Command**](iagentcommands--getcommand.md).

**Иаженткомманд** определяет интерфейс, позволяющий приложениям задавать и запрашивать свойства [**командных**](/windows/desktop/lwef/the-command-object) объектов, которые могут появляться во всплывающем меню символа и в окне "Voice Commands". Эти функции также доступны из [**иаженткоммандекс**](iagentcommandex.md). Объект **Command** — это элемент в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Сервер предоставляет пользователю доступ к командам, когда клиентское приложение переходит в активное входное значение.

[**Команда**](/windows/desktop/lwef/the-command-object) может присутствовать во всплывающем меню символа или в окне "голосовые команды". Для отображения во всплывающем меню он должен иметь [**заголовок**](caption-property.md) и иметь свойство [**Visible**](visible-property.md) со значением **true**. Для свойства **Visible** объекта коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) также должно быть задано **значение true** , чтобы команда отображалась во всплывающем меню, если клиентское приложение является входным. Для отображения в окне "команды с голосовыми командами" для **команды** должны быть заданы свойства [**воицекаптион**](voicecaption-property.md) и [**Voice**](voice-property.md) . (Для обеспечения обратной совместимости при отсутствии **воицекаптион** используется параметр **Caption** .)

При отображении меню записи всплывающего меню не меняются. При добавлении или удалении команд или изменении их свойств во время отображения всплывающего меню символа меню отображает эти изменения при повторном отображении. Однако в окне «Voice Commands» изменения отображаются по мере их выполнения.

В следующей таблице показано, как свойства команды влияют на ее представление.



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

Как правило, если вы определили [**команду**](/windows/desktop/lwef/the-command-object) с [**голосовым**](voice-property.md) параметром, вы также определяете параметры [**субтитров**](caption-property.md) и **голоса** для связанных коллекций [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Если коллекция **Commands** для набора команд не имеет **голоса** или не имеет параметра **заголовков** и в настоящий момент находится в активном состоянии, но **команды** имеют **субтитры** и параметры **голоса** , **команды** отображаются в представлении дерева окна "командные строки" в разделе "(неопределенная команда)", когда клиентское приложение становится входным.

Когда сервер получает входные данные, соответствующие одному из [**командных**](/windows/desktop/lwef/the-command-object) объектов, определенных для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) , он отправляет событие [**иажентнотифисинк:: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) и передает идентификатор команды в качестве атрибута объекта [**иажентусеринпут**](https://www.bing.com/search?q=**IAgentUserInput**) . Затем можно использовать условные операторы для сопоставления и обработки команды.

**Методы в порядке таблицы Vtable**



| Методы Иаженткомманд                                                   | Описание                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**сеткаптион**](https://www.bing.com/search?q=**SetCaption**)                             | Задает значение [**заголовка**](caption-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .                         |
| [**Субтитр**](https://www.bing.com/search?q=**GetCaption**)                             | Возвращает значение свойства [**Caption**](caption-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**сетвоице**](iagentcommand--setvoice.md)                             | Задает значение для текста [**голоса**](voice-property.md) для [**командного**](/windows/desktop/lwef/the-command-object) объекта.                        |
| [**Voice**](iagentcommand--getvoice.md)                             | Возвращает значение свойства [**Voice**](voice-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .                   |
| [**сетенаблед**](iagentcommand--setenabled.md)                         | Задает значение свойства [**Enabled**](enabled-property.md) для объекта [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Возвращает значение свойства [**Enabled**](enabled-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**сетвисибле**](iagentcommand--setvisible.md)                         | Задает значение свойства [**Visible**](visible-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .                 |
| [**Во всех видимых**](iagentcommand--getvisible.md)                         | Возвращает значение свойства [**Visible**](visible-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md) | Задает значение свойства [**достоверности**](confidence-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .           |
| [**жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md) | Возвращает значение свойства [**достоверности**](confidence-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) .         |
| [**сетконфиденцетекст**](iagentcommand--setconfidencetext.md)           | Задает значение свойства [**конфиденцетекст**](confidencetext-property.md) для объекта [**Command**](/windows/desktop/lwef/the-command-object) .   |
| [**жетконфиденцетекст**](iagentcommand--getconfidencetext.md)           | Возвращает значение свойства [**конфиденцетекст**](confidencetext-property.md) объекта [**Command**](/windows/desktop/lwef/the-command-object) . |
| [**getID**](iagentcommand--getid.md)                                   | Возвращает идентификатор объекта [**команды**](/windows/desktop/lwef/the-command-object) .                                                                      |



 

 

 