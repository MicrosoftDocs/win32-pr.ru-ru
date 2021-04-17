---
description: Вы можете создать объект для WMI в Visual Basic Scripting Edition (VBScript), подключившись к инструментарию WMI и вызывая CreateObject. В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Создание объекта с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497769"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="8aee3-104">Создание объекта с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="8aee3-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="8aee3-105">Вы можете создать объект для WMI в Visual Basic Scripting Edition (VBScript), подключившись к инструментарию WMI и вызывая [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8aee3-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="8aee3-106">В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.</span><span class="sxs-lookup"><span data-stu-id="8aee3-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="8aee3-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8aee3-107">Interface</span></span>                                        | <span data-ttu-id="8aee3-108">ProgID:</span><span class="sxs-lookup"><span data-stu-id="8aee3-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="8aee3-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="8aee3-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="8aee3-110">"Вбемскриптинг. SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="8aee3-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="8aee3-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="8aee3-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="8aee3-112">"Вбемскриптинг. SWbemLocator"</span><span class="sxs-lookup"><span data-stu-id="8aee3-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="8aee3-113">**свбемластеррор**</span><span class="sxs-lookup"><span data-stu-id="8aee3-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="8aee3-114">"Вбемскриптинг. SWbem. LastError"</span><span class="sxs-lookup"><span data-stu-id="8aee3-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="8aee3-115">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="8aee3-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="8aee3-116">"Вбемскриптинг. Свбемобжектпас"</span><span class="sxs-lookup"><span data-stu-id="8aee3-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="8aee3-117">**свбемнамедвалуесет**</span><span class="sxs-lookup"><span data-stu-id="8aee3-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="8aee3-118">"Вбемскриптинг. Свбемнамедвалуесет"</span><span class="sxs-lookup"><span data-stu-id="8aee3-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="8aee3-119">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="8aee3-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="8aee3-120">"Вбемскриптинг. Свбемрефрешер"</span><span class="sxs-lookup"><span data-stu-id="8aee3-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="8aee3-121">**свбемсинк**</span><span class="sxs-lookup"><span data-stu-id="8aee3-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="8aee3-122">"Вбемскриптинг. Свбемсинк"</span><span class="sxs-lookup"><span data-stu-id="8aee3-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="8aee3-123">В следующей процедуре описывается создание объекта WMI с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="8aee3-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="8aee3-124">**Создание объекта WMI с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="8aee3-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="8aee3-125">Подключитесь к инструментарию WMI с помощью моникера или объекта [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="8aee3-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="8aee3-126">Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="8aee3-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="8aee3-127">Выполните вызов метода [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript.</span><span class="sxs-lookup"><span data-stu-id="8aee3-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="8aee3-128">В следующем примере кода показано, как создать объект.</span><span class="sxs-lookup"><span data-stu-id="8aee3-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="8aee3-129">Если вы используете моникер на шаге 1, вам не нужно повторно вызывать функцию [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8aee3-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
