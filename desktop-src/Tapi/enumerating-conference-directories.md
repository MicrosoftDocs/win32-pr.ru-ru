---
description: В следующем фрагменте кода показано перечисление конференций на указанном сервере ILS. В этом фрагменте предполагается, что соединение с сервером ILS уже выполнено.
ms.assetid: da01c534-c700-4b4f-ac22-cede9930f80d
title: Перечисление каталогов конференций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eedffb44d92f52293dc9d1add8b53588503282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497811"
---
# <a name="enumerating-conference-directories"></a><span data-ttu-id="4ff0f-104">Перечисление каталогов конференций</span><span class="sxs-lookup"><span data-stu-id="4ff0f-104">Enumerating Conference Directories</span></span>

<span data-ttu-id="4ff0f-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4ff0f-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4ff0f-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4ff0f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4ff0f-107">В следующем фрагменте кода показано перечисление конференций на указанном сервере ILS.</span><span class="sxs-lookup"><span data-stu-id="4ff0f-107">The following code fragment illustrates the enumeration of conferences on a specified ILS server.</span></span> <span data-ttu-id="4ff0f-108">В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено.</span><span class="sxs-lookup"><span data-stu-id="4ff0f-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
SysFreeString( bNameToSearch );
```



## <a name="related-topics"></a><span data-ttu-id="4ff0f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4ff0f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ff0f-110">**иенумдиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="4ff0f-110">**IEnumDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)
</dt> </dl>

 

 



