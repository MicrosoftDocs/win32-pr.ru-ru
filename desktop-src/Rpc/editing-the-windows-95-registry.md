---
title: Изменение реестра Windows 95
description: С помощью Regedit можно изменить реестр Windows 95, указав NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889008"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="53fe2-103">Изменение реестра Windows 95</span><span class="sxs-lookup"><span data-stu-id="53fe2-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="53fe2-104">С помощью Regedit можно изменить реестр Windows 95, указав NSP.</span><span class="sxs-lookup"><span data-stu-id="53fe2-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="53fe2-105">**Назначение поставщика службы имен локатора Майкрософт для Windows 95**</span><span class="sxs-lookup"><span data-stu-id="53fe2-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="53fe2-106">Выберите пункт</span><span class="sxs-lookup"><span data-stu-id="53fe2-106">Select</span></span>

    <span data-ttu-id="53fe2-107">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="53fe2-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="53fe2-108">Создайте новый раздел с именем</span><span class="sxs-lookup"><span data-stu-id="53fe2-108">Create a new key called</span></span>

    <span data-ttu-id="53fe2-109">**намесервице**</span><span class="sxs-lookup"><span data-stu-id="53fe2-109">**NameService**</span></span>

3.  <span data-ttu-id="53fe2-110">Выбрав ключ **намесервице** , создайте новые имена **StringValue** и измените их, чтобы они содержали данные, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="53fe2-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="53fe2-111">Имя</span><span class="sxs-lookup"><span data-stu-id="53fe2-111">Name</span></span>                     | <span data-ttu-id="53fe2-112">Данные</span><span class="sxs-lookup"><span data-stu-id="53fe2-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="53fe2-113">**дефаултсинтакс**</span><span class="sxs-lookup"><span data-stu-id="53fe2-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="53fe2-114">3</span><span class="sxs-lookup"><span data-stu-id="53fe2-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="53fe2-115">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="53fe2-115">**Protocol**</span></span>             | <span data-ttu-id="53fe2-116">нкакн \_ NP</span><span class="sxs-lookup"><span data-stu-id="53fe2-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="53fe2-117">**Конечная точка**</span><span class="sxs-lookup"><span data-stu-id="53fe2-117">**Endpoint**</span></span>             | <span data-ttu-id="53fe2-118">\\\\указатель канала</span><span class="sxs-lookup"><span data-stu-id="53fe2-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="53fe2-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="53fe2-119">**NetworkAddress**</span></span>       | <span data-ttu-id="53fe2-120">MyServer (где MyServer — имя компьютера Windows NT)</span><span class="sxs-lookup"><span data-stu-id="53fe2-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="53fe2-121">**сервернетворкаддресс**</span><span class="sxs-lookup"><span data-stu-id="53fe2-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="53fe2-122">MyServer</span><span class="sxs-lookup"><span data-stu-id="53fe2-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="53fe2-123">С помощью Regedit можно изменить реестр Windows 95, чтобы назначить компакт-диски DCE NSP.</span><span class="sxs-lookup"><span data-stu-id="53fe2-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="53fe2-124">**Назначение поставщика службы имен дисков DCE для Windows 95**</span><span class="sxs-lookup"><span data-stu-id="53fe2-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="53fe2-125">Выберите пункт</span><span class="sxs-lookup"><span data-stu-id="53fe2-125">Select</span></span>

    <span data-ttu-id="53fe2-126">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="53fe2-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="53fe2-127">Создайте новый раздел с именем</span><span class="sxs-lookup"><span data-stu-id="53fe2-127">Create a new key called</span></span>

    <span data-ttu-id="53fe2-128">**намесервице**</span><span class="sxs-lookup"><span data-stu-id="53fe2-128">**NameService**</span></span>

3.  <span data-ttu-id="53fe2-129">Выбрав ключ **намесервице** , создайте новые имена **StringValue** и измените их, чтобы они содержали данные, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="53fe2-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="53fe2-130">Имя</span><span class="sxs-lookup"><span data-stu-id="53fe2-130">Name</span></span>                     | <span data-ttu-id="53fe2-131">Данные</span><span class="sxs-lookup"><span data-stu-id="53fe2-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="53fe2-132">**дефаултсинтакс**</span><span class="sxs-lookup"><span data-stu-id="53fe2-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="53fe2-133">3</span><span class="sxs-lookup"><span data-stu-id="53fe2-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="53fe2-134">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="53fe2-134">**Protocol**</span></span>             | <span data-ttu-id="53fe2-135">нкакн \_ IP \_ TCP</span><span class="sxs-lookup"><span data-stu-id="53fe2-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="53fe2-136">**Конечная точка**</span><span class="sxs-lookup"><span data-stu-id="53fe2-136">**Endpoint**</span></span>             | <span data-ttu-id="53fe2-137">"" (пустая строка)</span><span class="sxs-lookup"><span data-stu-id="53fe2-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="53fe2-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="53fe2-138">**NetworkAddress**</span></span>       | <span data-ttu-id="53fe2-139">MyServer (имя главного компьютера, на котором работает нсид)</span><span class="sxs-lookup"><span data-stu-id="53fe2-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="53fe2-140">**сервернетворкаддресс**</span><span class="sxs-lookup"><span data-stu-id="53fe2-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="53fe2-141">MyServer (имя главного компьютера, на котором работает нсид)</span><span class="sxs-lookup"><span data-stu-id="53fe2-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="53fe2-142">Для настройки компакт-дисков DCE в качестве поставщика службы имен требуется продукт службы каталогов компании DCE Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="53fe2-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="53fe2-143">Сведения о компакт-дисках DCE см. в документации, предоставляемой корпорацией Digital Equipment.</span><span class="sxs-lookup"><span data-stu-id="53fe2-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





