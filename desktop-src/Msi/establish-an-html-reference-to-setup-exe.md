---
description: Последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в примере установки установщик Windows на основе URL-адреса.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Установка ссылки HTML на Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264848"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="43174-103">Установка ссылки HTML на Setup.exe</span><span class="sxs-lookup"><span data-stu-id="43174-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="43174-104">Последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в [примере установки установщик Windows на основе URL-адреса](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="43174-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="43174-105">Используйте следующий скрипт HTML:</span><span class="sxs-lookup"><span data-stu-id="43174-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="43174-106">Если щелкнуть ссылку "Установка MySetup", пользователи смогут сохранить или запустить из этого расположения.</span><span class="sxs-lookup"><span data-stu-id="43174-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="43174-107">Если пользователь выбирает Запуск из этого расположения, Setup.exe обновляет версию установщик Windows на компьютере, при необходимости проверяет цифровую подпись в пакете установщика и устанавливает пакет на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="43174-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="43174-108">Это завершает пример.</span><span class="sxs-lookup"><span data-stu-id="43174-108">This completes the example.</span></span>

 

 



