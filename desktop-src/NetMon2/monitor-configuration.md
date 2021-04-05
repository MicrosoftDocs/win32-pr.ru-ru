---
description: Мониторы можно настроить с помощью пользовательского интерфейса сетевой монитор. Конечные пользователи могут передавать критерии конфигурации в монитор с помощью HTML-формы, хранящейся в виде файла HTM, в следующей вложенной папке установленного сетевой монитор SDK.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Конфигурация монитора (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991204"
---
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="6492b-104">Конфигурация монитора (сетевой монитор)</span><span class="sxs-lookup"><span data-stu-id="6492b-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="6492b-105">Мониторы можно настроить с помощью пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="6492b-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="6492b-106">Конечные пользователи могут передавать критерии конфигурации в монитор с помощью HTML-формы, хранящейся в виде файла HTM, в следующей вложенной папке установленного сетевой монитор SDK.</span><span class="sxs-lookup"><span data-stu-id="6492b-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="6492b-107">Когда пользователь выбирает кнопку **Set Monitor Configuration (настроить монитор конфигурации** ), браузер создает сообщение HTML **POST** , содержащее имена и значения всех элементов HTML-форм.</span><span class="sxs-lookup"><span data-stu-id="6492b-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="6492b-108">Когда МКСВК вызывает метод [имонитор::D оконфигуре](imonitor-doconfigure.md) , параметр *пконфигуратион* указывает на данные из сообщения POST.</span><span class="sxs-lookup"><span data-stu-id="6492b-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="6492b-109">В следующем примере кода приведен пример данных сообщения POST:</span><span class="sxs-lookup"><span data-stu-id="6492b-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Эти данные передаются в виде длинной строки ASCII. Строка выглядит довольно необычная, как для ее длины, так и для внешнего вида таких разделов, как% 3A% 5C и% 0D% 0A. Это пекулиарити вызвано HTML, что требует, чтобы метод поместил все возможные строки ANSI, DBCS и Юникод в формат ASCII. Например, метод **доконфигуре** вставляет определенные символы, такие как амперсанд (&), перед именем переменной, чтобы обозначить ее как имя переменной. % 3A% 5C является закодированной формой символа двоеточия, а% 0D% 0A указывает пару "возврат каретки/перевод строки". <span data-ttu-id="6492b-115">Следующий пример кода предоставляет полученный код HTML, интерпретируемый монитором.</span><span class="sxs-lookup"><span data-stu-id="6492b-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



