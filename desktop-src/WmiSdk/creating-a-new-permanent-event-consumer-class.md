---
description: Одним из первых шагов при создании постоянного потребителя событий является создание класса WMI, который описывает потребителя событий. В частности, класс постоянных потребителей событий определяет параметры действия, реализуемого физическим потребителем.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Создание нового класса постоянного потребителя событий
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711744"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="d2ca5-104">Создание нового класса постоянного потребителя событий</span><span class="sxs-lookup"><span data-stu-id="d2ca5-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="d2ca5-105">Одним из первых шагов при создании постоянного потребителя событий является создание класса WMI, который описывает потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="d2ca5-106">В частности, класс постоянных потребителей событий определяет параметры действия, реализуемого физическим потребителем.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="d2ca5-107">В следующей процедуре описывается создание класса постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="d2ca5-108">**Создание класса постоянного потребителя событий**</span><span class="sxs-lookup"><span data-stu-id="d2ca5-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="d2ca5-109">Создайте класс, производный от класса System [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ca5-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="d2ca5-110">Реализуйте все параметры, необходимые для обработки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="d2ca5-111">В следующем примере показан синтаксис, используемый для создания класса Смтпконсумеревент.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="d2ca5-112">Это можно использовать в качестве примера для создания нового класса.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="d2ca5-113">Класс [**смтпевентконсумер**](smtpeventconsumer.md) отправляет сообщение электронной почты с помощью протокола SMTP каждый раз, когда в него передается событие.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="d2ca5-114">Этот класс определен в смтпконс. mof.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-114">This class is defined in smtpcons.mof.</span></span>

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

<span data-ttu-id="d2ca5-115">Вы должны иметь возможность создавать экземпляры класса постоянных потребителей событий, чтобы описать один или несколько способов отправки событий физическому потребителю.</span><span class="sxs-lookup"><span data-stu-id="d2ca5-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="d2ca5-116">Дополнительные сведения см. [в разделе Создание логического потребителя](creating-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="d2ca5-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



