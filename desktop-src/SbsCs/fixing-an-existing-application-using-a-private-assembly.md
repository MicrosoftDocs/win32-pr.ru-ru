---
description: Начиная с Windows XP, можно создать закрытую сборку и сделать ее доступной для конкретного приложения.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Исправление существующего приложения с помощью закрытой сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072688"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="9a757-103">Исправление существующего приложения с помощью закрытой сборки</span><span class="sxs-lookup"><span data-stu-id="9a757-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="9a757-104">Начиная с Windows XP, можно создать закрытую сборку и сделать ее доступной для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="9a757-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="9a757-105">Эту возможность можно использовать для исправления приложения, которое станет несовместимым с обновлением.</span><span class="sxs-lookup"><span data-stu-id="9a757-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="9a757-106">Примером может быть приложение, которое станет несовместимым с последней версией MSVCRT.DLL после обновления операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9a757-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="9a757-107">В этом случае нет возможности заменить версию системы, так как MSVCRT.DLL является защищенным файлом Windows.</span><span class="sxs-lookup"><span data-stu-id="9a757-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="9a757-108">Вместо того чтобы переписывать приложение для работы с новой версией MSVCRT, можно создать закрытую сборку для MSVCRT и установить ее в папке приложения.</span><span class="sxs-lookup"><span data-stu-id="9a757-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="9a757-109">Обратите внимание, что не каждый общий компонент является подходящим кандидатом для закрытой параллельной сборки, а некоторые компоненты имеют ограничения лицензирования относительно того, где можно установить компоненты.</span><span class="sxs-lookup"><span data-stu-id="9a757-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="9a757-110">Компонент должен удовлетворять критериям для параллельного компонента.</span><span class="sxs-lookup"><span data-stu-id="9a757-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="9a757-111">Обратитесь к издателю компонента, если он может предоставить подходящую сборку.</span><span class="sxs-lookup"><span data-stu-id="9a757-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="9a757-112">Манифест закрытой сборки и манифест приложения должны быть установлены в той же папке, что и исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="9a757-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="9a757-113">При запуске приложения он обращается к манифесту приложения и загружает версию MSVCRT, которая является частной для приложения.</span><span class="sxs-lookup"><span data-stu-id="9a757-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="9a757-114">В этом примере частная сборка будет включать как MSVCRT.DLL, так и MSVCIRT.DLL, как в следующем манифесте сборки:</span><span class="sxs-lookup"><span data-stu-id="9a757-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="9a757-115">Ниже приведен пример возможного манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="9a757-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



