---
description: Логический потребитель — это экземпляр класса постоянного потребителя событий.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Создание логического потребителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712773"
---
# <a name="creating-a-logical-consumer"></a><span data-ttu-id="2b308-103">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="2b308-103">Creating a Logical Consumer</span></span>

<span data-ttu-id="2b308-104">Логический потребитель — это экземпляр класса постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="2b308-104">A logical consumer is an instance of a permanent event consumer class.</span></span> <span data-ttu-id="2b308-105">Основное назначение логического потребителя — предоставить физическому потребителю параметры для действий, выполняемых физическим потребителем.</span><span class="sxs-lookup"><span data-stu-id="2b308-105">The main purpose of a logical consumer is to provide the physical consumer with the parameters for the activities the physical consumer performs.</span></span> <span data-ttu-id="2b308-106">Дополнительные сведения см. [в разделе Создание нового класса постоянного потребителя событий](creating-a-new-permanent-event-consumer-class.md).</span><span class="sxs-lookup"><span data-stu-id="2b308-106">For more information, see [Creating a New Permanent Event Consumer Class](creating-a-new-permanent-event-consumer-class.md).</span></span> <span data-ttu-id="2b308-107">Постоянный потребитель должен иметь тот же [**креаторсид**](--eventconsumer.md) в экземплярах объекта-получателя, фильтра и привязки.</span><span class="sxs-lookup"><span data-stu-id="2b308-107">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="2b308-108">Дополнительные сведения см. в статье [безопасное получение событий](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="2b308-108">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span> <span data-ttu-id="2b308-109">Пример использования логического потребителя см. в разделе [выполнение скрипта на основе события](running-a-script-based-on-an-event.md), в котором показано использование стандартного класса потребителя [**активескриптевентконсумер**](activescripteventconsumer.md) для настройки постоянного потребителя.</span><span class="sxs-lookup"><span data-stu-id="2b308-109">For an example of using a logical consumer, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md), which shows the use of the standard consumer class [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to configure a permanent consumer.</span></span>

<span data-ttu-id="2b308-110">В следующей процедуре описывается создание логического потребителя.</span><span class="sxs-lookup"><span data-stu-id="2b308-110">The following procedure describes how to create a logical consumer.</span></span>

<span data-ttu-id="2b308-111">**Создание логического потребителя**</span><span class="sxs-lookup"><span data-stu-id="2b308-111">**To create a logical consumer**</span></span>

1.  <span data-ttu-id="2b308-112">Создайте экземпляр класса постоянного потребителя.</span><span class="sxs-lookup"><span data-stu-id="2b308-112">Create an instance of your permanent consumer class.</span></span>
2.  <span data-ttu-id="2b308-113">Заполните свойства экземпляра параметрами действия, которое должен выполнить физический потребитель.</span><span class="sxs-lookup"><span data-stu-id="2b308-113">Fill the properties of the instance with the parameters of the action you want the physical consumer to perform.</span></span>

<span data-ttu-id="2b308-114">В следующем примере кода MOF описывается логический потребитель, содержащий скрипт.</span><span class="sxs-lookup"><span data-stu-id="2b308-114">The following MOF code example describes a logical consumer that contains a script.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="2b308-115">После создания логического потребителя необходимо связать каждый фильтр с фильтром событий, чтобы назначить действие конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="2b308-115">After you create the logical consumer, you must then link each filter to an event filter to assign the action to a particular event.</span></span> <span data-ttu-id="2b308-116">Дополнительные сведения см. в разделе [Создание фильтра событий](creating-an-event-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2b308-116">For more information, see [Creating an Event Filter](creating-an-event-filter.md).</span></span>

 

 



