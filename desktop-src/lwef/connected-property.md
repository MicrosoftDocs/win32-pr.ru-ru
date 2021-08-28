---
title: Подключенное свойство
description: Подключенное свойство
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19326f7770bbd4a42f6ff66a4517cd6151f3c54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884923"
---
# <a name="connected-property"></a>Подключенное свойство

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает или задает значение, указывающее, подключен ли текущий элемент управления к серверу Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*агент. * * подключен* *  \[  =  *логическое значение*\]



| Часть      | Описание                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Логическое выражение, указывающее, подключен ли элемент управления. **Значение true** Элемент управления подключен.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Во многих случаях при указании элемента управления автоматически создается подключение к серверу Microsoft Agent. Например, при указании идентификатора CLSID элемента управления Microsoft Agent в &lt; &gt; теге объекта на веб-странице автоматически открывается соединение с сервером, а при выходе из страницы закрывается соединение. аналогичным образом, для Visual Basic или других языков, позволяющих удалить элемент управления в форме, при запуске программы автоматически открывается подключение, и при выходе из программы закрывается подключение. Если сервер в данный момент не запущен, он запускается автоматически.

Однако если вы хотите создать элемент управления агента во время выполнения, вам также может потребоваться явно открыть новое соединение с сервером с помощью свойства **Connected** . например, в Visual Basic во время выполнения можно создать объект ActiveX, используя инструкцию Set с ключевым словом **New** (или CreateObject function). При этом создается объект, который не может создать соединение с сервером. Можно использовать свойство **Connected** перед любым кодом, который вызывает интерфейс программирования Microsoft Agent, как показано в следующем примере:


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



Создание элемента управления с помощью этого метода не предоставляет события элемента управления агента. в Visual Basic 5,0 (и более поздних версиях) можно получить доступ к событиям элемента управления, включив элемент управления в ссылки проекта, и использовать ключевое слово **withevents** в объявлении переменной:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



При использовании **WithEvents** для создания экземпляра элемента управления агента во время выполнения автоматически открывается подключение к серверу Microsoft Agent. Поэтому нет необходимости включать **подключенную** инструкцию.

Можно закрыть подключение к серверу, освобождая все созданные ссылки на объекты агента, такие как Иажентктлчарактерекс и Иажентктлкоммандекс. Необходимо также освободить ссылку на сам элемент управления агента. в Visual Basic можно освободить ссылку на объект, присвоив его переменной значение **Nothing**. Если вы загрузили символы, выгрузите их перед освобождением объекта символов.


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> Невозможно закрыть подключение к серверу, освобождая ссылки, в которых был добавлен компонент. например, невозможно закрыть подключение к серверу на веб-страницах, где используется &lt; &gt; тег объекта для объявления элемента управления или в Visual Basic приложении, в котором элемент управления перекрывается в форме. При освобождении всех ссылок на агенты будет уменьшен рабочий набор агента, подключение останется до перехода на следующую страницу или выхода из приложения.

 

 

 





