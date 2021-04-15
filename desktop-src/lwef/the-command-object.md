---
title: Объект Command
description: Объект Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710275"
---
# <a name="the-command-object"></a>Объект Command

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**Command**](/windows/desktop/lwef/the-command-object) — это элемент в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Сервер предоставляет пользователю доступ к объектам **команды** , когда клиентское приложение преобразуется в входные данные.

-   [Свойства объекта Command](command-object-properties.md)

Чтобы получить доступ к свойству объекта [**Command**](/windows/desktop/lwef/the-command-object) , вы ссылаетесь на него в своей коллекции, используя свойство [**Name**](name-property.md) . В VBScript и Visual Basic можно использовать свойство **Name** напрямую:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Для языков программирования, которые не поддерживают коллекции, используйте [**Командный**](command-method.md) метод:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Вы также можете ссылаться на объект Command, создав ссылку на него. В Visual Basic объявите объектную переменную и используйте инструкцию SET для создания ссылки:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



В Visual Basic 5,0 можно также объявить объект как тип [**иажентктлкоммандекс**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) и создать ссылку. Это соглашение включает раннее связывание, что приводит к лучшей производительности:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



В VBScript можно объявить ссылку как конкретный тип, но вы по-прежнему можете объявить переменную и задать ее для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Команда может отображаться во всплывающем меню символа, в окне команд или в обоих окнах. Для отображения во всплывающем меню он должен иметь заголовок и иметь свойство [**Visible**](visible-property.md) со значением **true**. Кроме того, свойство **Visible** объекта коллекции Commands также должно иметь значение **true**. Для отображения в окне команды в [**команде**](/windows/desktop/lwef/the-command-object) должны быть заданы свойства [**Caption**](caption-property.md) и [**Voice**](voice-property.md) . Обратите внимание, что во время отображения меню записи всплывающего меню не меняются. При добавлении или удалении команд или изменении их свойств во время отображения всплывающего меню символа меню отображает эти изменения при каждом отображении пользователем. Однако окно команды динамически отражает любые внесенные изменения.

В следующей таблице показано, как свойства [**команды**](/windows/desktop/lwef/the-command-object) влияют на ее представление.



Свойство Caption

Voice-Caption, свойство

Свойство Voice

Свойство Visible

Свойство Enabled

Отображается во всплывающем меню "символ"

Отображается в окне "команды"

Да

Да

Да

True

True

Обычная, использование [ **подписи**](caption-property.md)

Да, с помощью [ **воицекаптион**](voicecaption-property.md)

Да

Да

Да

True

Неверно

Отключено, используется [ **заголовок**](caption-property.md)

Нет

Да

Да

Да

False

True

Не отображается

Да, с помощью [ **воицекаптион**](voicecaption-property.md)

Да

Да

Да

Неверно

False

Не отображается

Нет

Да

Да

Нет 

True

True

Обычная, использование [ **подписи**](caption-property.md)

Нет

Да

Да

Нет 

True

Неверно

Отключено, используется [ **заголовок**](caption-property.md)

Нет

Да

Да

Нет 

False

True

Не отображается

Нет

Да

Да

Нет 

Неверно

False

Не отображается

Нет

Нет 

Да

Да

True

True

Не отображается

Да, с помощью [ **воицекаптион**](voicecaption-property.md)

Нет 

Да

Да

True

Неверно

Не отображается

Нет

Нет 

Да

Да

False

True

Не отображается

Да, с помощью [ **воицекаптион**](voicecaption-property.md)

Нет 

Да

Да

Неверно

False

Не отображается

Нет

Нет 

Да

Нет 

True

True

Не отображается

Нет

Нет 

Да

Нет 

True

Неверно

Не отображается

Нет

Нет 

Да

Нет 

False

True

Не отображается

Нет

Нет 

Да

Нет 

Неверно

False

Не отображается

Нет

Да

Нет 

Да

True

True

Обычная, использование [ **подписи**](caption-property.md)

Да, с использованием [ **заголовка**](caption-property.md)

Да

Нет 

Да

True

Неверно

Отключено, используется [ **заголовок**](caption-property.md)

Нет

Да

Нет 

Да

False

True

Не отображается

Да, с использованием [ **заголовка**](caption-property.md)

Да

Нет 

Да

Неверно

False

Не отображается

Нет

Да

Нет 

Нет 

True

True

Обычная, использование [ **подписи**](caption-property.md)

Нет

Да

Нет 

Нет 

True

Неверно

Отключено, используется [ **заголовок**](caption-property.md)

Нет

Да

Нет 

Нет 

False

True

Не отображается

Нет

Да

Нет 

Нет 

Неверно

False

Не отображается

Нет

Нет 

Нет 

Да

True

True

Не отображается

Нет 

Нет 

Нет 

Да

True

Неверно

Не отображается

Нет

Нет 

Нет 

Да

False

True

Не отображается

Нет 

Нет 

Нет 

Да

Неверно

False

Не отображается

Нет

Нет 

Нет 

Нет 

True

True

Не отображается

Нет

Нет 

Нет 

Нет 

True

Неверно

Не отображается

Нет

Нет 

Нет 

Нет 

False

True

Не отображается

Нет

Нет 

Нет 

Нет 

Неверно

False

Не отображается

Нет

 Значение, если значение свойства равно null. В некоторых языках программирования пустая строка не может интерпретироваться как строка со значением NULL.  Команда по-прежнему доступна для передачи голоса.<br/>



 

Когда сервер получает входные данные для одной из команд, он отправляет [**командное**](/windows/desktop/lwef/the-command-object) событие и передает имя **команды** в виде атрибута объекта [**UserInput**](/windows/desktop/lwef/iagentuserinput) . Затем можно использовать условные операторы для сопоставления и обработки **команды**.

 

