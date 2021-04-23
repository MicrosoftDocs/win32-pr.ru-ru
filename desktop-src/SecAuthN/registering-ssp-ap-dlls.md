---
description: После разработки библиотеки динамической компоновки (SSP или AP DLL), содержащей один или несколько настраиваемых пакетов безопасности, необходимо зарегистрировать их.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Регистрация DLL-библиотек SSP и AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813592"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="003ce-103">Регистрация DLL-библиотек SSP и AP</span><span class="sxs-lookup"><span data-stu-id="003ce-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="003ce-104">После разработки [](../secgloss/s-gly.md) / библиотеки динамической компоновки [*пакета проверки подлинности*](../secgloss/a-gly.md) поставщика поддержки безопасности (SSP/AP DLL), содержащей один или несколько пользовательских [*пакетов безопасности*](../secgloss/s-gly.md), необходимо зарегистрировать их.</span><span class="sxs-lookup"><span data-stu-id="003ce-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="003ce-105">Для этого добавьте имя настраиваемой библиотеки DLL или объекта AP в данные следующего значения реестра:</span><span class="sxs-lookup"><span data-stu-id="003ce-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="003ce-106">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **Управление** \\  \\ **пакетами безопасности** LSA</span><span class="sxs-lookup"><span data-stu-id="003ce-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="003ce-107">Данные для этого значения реестра представляют собой список имен DLL-библиотек SSP и AP без расширения ". dll".</span><span class="sxs-lookup"><span data-stu-id="003ce-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="003ce-108">Тип данных этого списка — **reg \_ Multi \_ SZ** , поэтому для \\ каждого имени библиотеки DLL в списке должен быть задан символ null ("0").</span><span class="sxs-lookup"><span data-stu-id="003ce-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="003ce-109">Как правило, DLL-библиотеки SSP и AP хранятся в каталоге% SystemRoot%/System32.</span><span class="sxs-lookup"><span data-stu-id="003ce-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="003ce-110">Если это путь к настраиваемой библиотеке поставщика общих служб (DLL), то не включайте путь как часть имени библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="003ce-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="003ce-111">Однако если библиотека DLL находится в другом пути, включите полный путь к библиотеке DLL в имени.</span><span class="sxs-lookup"><span data-stu-id="003ce-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="003ce-112">При каждом запуске системы LSA загружает в этот список DLL-библиотеки SSP/AP и выполняет последовательность инициализации, описанную в разделе [инициализация в режиме LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="003ce-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="003ce-113">Регистрация настраиваемого пакета безопасности в качестве поставщика общих служб TLS по умолчанию</span><span class="sxs-lookup"><span data-stu-id="003ce-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="003ce-114">После разработки настраиваемого поставщика поддержки безопасности TLS и его регистрации, как описано выше, необходимо также зарегистрировать его в качестве "поставщика службы TLS по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="003ce-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="003ce-115">Для этого заполните Имя пакета пользовательского поставщика общих служб данными следующего значения реестра:</span><span class="sxs-lookup"><span data-stu-id="003ce-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="003ce-116">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **Управление** \\ **LSA** \\ **по умолчанию SSP TLS**</span><span class="sxs-lookup"><span data-stu-id="003ce-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="003ce-117">Данные этого значения реестра — это имя пакета SSP, а не имя библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="003ce-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="003ce-118">Для этого используется следующий тип данных: **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="003ce-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="003ce-119">Приложения пользовательского режима, использующие "Стандартный TLS SSP", будут использовать зарегистрированную здесь по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="003ce-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="003ce-120">Это изменение не повлияет на приложения режима ядра или приложения, используемые в пользовательском режиме, использующие "поставщик Microsoft Unified Security Protocol" или другие конкретные имена SSP TLS.</span><span class="sxs-lookup"><span data-stu-id="003ce-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="003ce-121">Эти сведения о реестре относятся только к библиотеке DLL поставщика общих служб и AP.</span><span class="sxs-lookup"><span data-stu-id="003ce-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="003ce-122">Сведения о регистрации поставщиков поддержки безопасности (SSP) см. [в статье написание и установка поставщика поддержки безопасности](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="003ce-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="003ce-123">Сведения о различиях между библиотеками DLL SSP/AP и SSP см. в разделе [SSP/ТД/SSP](ssp-aps-versus-ssps.md).</span><span class="sxs-lookup"><span data-stu-id="003ce-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="003ce-124">См. также</span><span class="sxs-lookup"><span data-stu-id="003ce-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="003ce-125">Ограничения, касающихся регистрации и установки пакета безопасности</span><span class="sxs-lookup"><span data-stu-id="003ce-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
