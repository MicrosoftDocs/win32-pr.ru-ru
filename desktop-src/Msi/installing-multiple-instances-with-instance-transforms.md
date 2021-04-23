---
description: В этом разделе приводятся рекомендации по установке или переустановке нескольких экземпляров, использующих преобразования экземпляра.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Установка нескольких экземпляров с преобразованиями экземпляров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080419"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="4dc3c-103">Установка нескольких экземпляров с преобразованиями экземпляров</span><span class="sxs-lookup"><span data-stu-id="4dc3c-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="4dc3c-104">В этом разделе приводятся рекомендации по установке или переустановке нескольких экземпляров, использующих преобразования экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="4dc3c-105">При установке нового экземпляра с преобразованием экземпляра Включите свойство **мсиневинстанце** и задайте **мсиневинстанце**= 1.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="4dc3c-106">При установке нового экземпляра с преобразованием экземпляра Включите свойство Transforms и установите первое преобразование в списке преобразований в преобразование экземпляра, которое изменяет код продукта.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="4dc3c-107">Все преобразования настройки должны следовать за преобразованием экземпляра в начале этого списка.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="4dc3c-108">Самым простым способом запуска установки обслуживания и переустановки экземпляра является ссылка на код продукта экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="4dc3c-109">При запуске установки обслуживания с помощью пути к пакету необходимо также указать код продукта экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="4dc3c-110">В командной строке используйте параметр/n {код продукта}.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="4dc3c-111">Из кода или скрипта используйте свойство **мсиинстанцегуид** .</span><span class="sxs-lookup"><span data-stu-id="4dc3c-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="4dc3c-112">В следующем примере показано, как установить новый экземпляр из командной строки, в которой преобразование экземпляра предваряется двоеточием, указывающим, что преобразование внедрено в пакет.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="4dc3c-113">**msiexec/I mypackage.msi преобразования =: instance. MST МСИНЕВИНСТАНЦЕ = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="4dc3c-114">В следующем примере показано, как установить новый экземпляр с помощью [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="4dc3c-115">В следующем примере показано, как установить новый экземпляр из скрипта.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="4dc3c-116">В следующем примере переустанавливается экземпляр без повторного кэширования пакета.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="4dc3c-117">На экземпляр ссылается его код продукта {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="4dc3c-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="4dc3c-118">**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="4dc3c-119">В следующем примере переустанавливается экземпляр и повторно кэшируется пакет из командной строки.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="4dc3c-120">На экземпляр ссылается путь пакета.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="4dc3c-121">Если продукт изначально установлен с преобразованием экземпляра, необходимо указать только параметр/n {код продукта}.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="4dc3c-122">**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus REINSTALL/QB**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="4dc3c-123">В следующем примере переустанавливается экземпляр и кэшируется пакет с помощью **мсиинсталлпродукт**.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="4dc3c-124">На экземпляр ссылается путь пакета.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="4dc3c-125">Используйте свойство **мсиинстанцегуид** для предоставления кода продукта экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="4dc3c-126">В следующем примере переустанавливается экземпляр и кэшируется пакет с помощью скрипта.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="4dc3c-127">Используйте свойство **мсиинстанцегуид** для предоставления кода продукта экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="4dc3c-128">В следующем примере показано, как объявить экземпляр с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="4dc3c-129">**msiexec/жм mypackage.msi/t: instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="4dc3c-130">В следующем примере показано, как установить, чтобы объявить экземпляр с помощью **мсиадвертисепродуктекс**.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="4dc3c-131">В следующем примере показано, как применить исправление к экземпляру из командной строки.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="4dc3c-132">Если продукт изначально был установлен с преобразованием экземпляра, необходимо включить параметр/n {код продукта}.</span><span class="sxs-lookup"><span data-stu-id="4dc3c-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="4dc3c-133">**msiexec/p мипатч. MSP/n {00000001-0002-0000-0000-624474736554} /QB**</span><span class="sxs-lookup"><span data-stu-id="4dc3c-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="4dc3c-134">В следующем примере показано, как применить исправление к экземпляру установки с помощью [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="4dc3c-135">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md) и [Создание нескольких экземпляров с помощью преобразований экземпляров](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4dc3c-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



