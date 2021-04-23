---
description: Со временем могут быть созданы различные версии TAPI, приложений и поставщиков служб.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Управление версиями TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346785"
---
# <a name="tapi-versioning"></a><span data-ttu-id="32187-103">Управление версиями TAPI</span><span class="sxs-lookup"><span data-stu-id="32187-103">TAPI Versioning</span></span>

<span data-ttu-id="32187-104">Со временем могут быть созданы различные версии TAPI, приложений и поставщиков служб.</span><span class="sxs-lookup"><span data-stu-id="32187-104">Over time, different versions of TAPI, applications, and service providers may be produced.</span></span> <span data-ttu-id="32187-105">Эти новые версии могут создавать новые определения, например для новых функций, новых элементов в структурах данных и новых битовых полей.</span><span class="sxs-lookup"><span data-stu-id="32187-105">These new versions can make new definitions, such as for new features, new members in data structures, and new bit fields.</span></span> <span data-ttu-id="32187-106">Следовательно, Номера версий необходимы для указания способа интерпретации различных структур данных.</span><span class="sxs-lookup"><span data-stu-id="32187-106">Version numbers are therefore necessary to indicate how to interpret various data structures.</span></span>

<span data-ttu-id="32187-107">Чтобы обеспечить оптимальное взаимодействие различных версий приложений, версий самой TAPI и версий поставщиков услуг разных поставщиков, Microsoft телефонии предоставляет простой механизм согласования версий для приложений.</span><span class="sxs-lookup"><span data-stu-id="32187-107">To allow optimal interoperability of different versions of applications, versions of TAPI itself, and versions of service providers by different vendors, Microsoft Telephony provides a simple version negotiation mechanism for applications.</span></span> <span data-ttu-id="32187-108">Существует две различные версии, которые TAPI и поставщик услуг телефонии должны согласовать для каждого устройства линии.</span><span class="sxs-lookup"><span data-stu-id="32187-108">There are two different versions that TAPI and the telephony service provider need to agree on for each line device.</span></span> <span data-ttu-id="32187-109">Первая — это версия, согласованная с TAPI и поставщиком услуг телефонии (TSP) Basic и дополнительная телефония, называемая версией интерфейса TAPI.</span><span class="sxs-lookup"><span data-stu-id="32187-109">The first is the version negotiated with TAPI and the telephony service provider (TSP) Basic and Supplementary Telephony, referred to as the TAPI interface version.</span></span> <span data-ttu-id="32187-110">Другой — для расширений, зависящих от поставщика, если таковые имеются, и называется версией расширения.</span><span class="sxs-lookup"><span data-stu-id="32187-110">The other is for provider-specific extensions, if any, and is referred to as the extension version.</span></span> <span data-ttu-id="32187-111">Формат структур данных и типов данных, используемых базовыми и дополнительными функциями TAPI, определяется версией TAPI, а версия расширения определяет формат структур данных, определенных расширениями, определенными для поставщика.</span><span class="sxs-lookup"><span data-stu-id="32187-111">The format of the data structures and data types used by TAPI's Basic and Supplementary features is defined by the TAPI version, while the extension version determines the format of data structures defined by the vendor-specific extensions.</span></span>

<span data-ttu-id="32187-112">Функция [**линенеготиатеапиверсион**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) СОГЛАСОВЫВАЕТ версию TAPI и [**линенеготиатикстверсион**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) согласовывает версию расширения TSP.</span><span class="sxs-lookup"><span data-stu-id="32187-112">The [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) function negotiates a TAPI version and [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negotiates the TSP extension version.</span></span> <span data-ttu-id="32187-113">Один TSP может обрабатывать более одной версии, и приложение должно "возвращаться" к использованию более старой версии, если используется более старая версия TSP.</span><span class="sxs-lookup"><span data-stu-id="32187-113">A single TSP could be capable of handling more than one version, and an application must "fall back" to using an older version if using an older TSP.</span></span> <span data-ttu-id="32187-114">В **линенеготиатеапиверсион** параметр *двапиверсион* по умолчанию имеет значение в соответствии с версией, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="32187-114">In **lineNegotiateAPIVersion** the *dwApiVersion* parameter defaults to a value according to version, as follows.</span></span>



| <span data-ttu-id="32187-115">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="32187-115">TAPI version</span></span> | <span data-ttu-id="32187-116">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="32187-116">Default value</span></span> |
|--------------|---------------|
| <span data-ttu-id="32187-117">1,3</span><span class="sxs-lookup"><span data-stu-id="32187-117">1.3</span></span>          | <span data-ttu-id="32187-118">0x00010003</span><span class="sxs-lookup"><span data-stu-id="32187-118">0x00010003</span></span>    |
| <span data-ttu-id="32187-119">1.4</span><span class="sxs-lookup"><span data-stu-id="32187-119">1.4</span></span>          | <span data-ttu-id="32187-120">0x00010004</span><span class="sxs-lookup"><span data-stu-id="32187-120">0x00010004</span></span>    |
| <span data-ttu-id="32187-121">2.0</span><span class="sxs-lookup"><span data-stu-id="32187-121">2.0</span></span>          | <span data-ttu-id="32187-122">0x00020000</span><span class="sxs-lookup"><span data-stu-id="32187-122">0x00020000</span></span>    |
| <span data-ttu-id="32187-123">2.1</span><span class="sxs-lookup"><span data-stu-id="32187-123">2.1</span></span>          | <span data-ttu-id="32187-124">0x00020001</span><span class="sxs-lookup"><span data-stu-id="32187-124">0x00020001</span></span>    |
| <span data-ttu-id="32187-125">2.2</span><span class="sxs-lookup"><span data-stu-id="32187-125">2.2</span></span>          | <span data-ttu-id="32187-126">0x00020002</span><span class="sxs-lookup"><span data-stu-id="32187-126">0x00020002</span></span>    |



 

<span data-ttu-id="32187-127">Тем не менее TAPI делает это гораздо проще, если сам TSP использует более новую версию, чем приложение.</span><span class="sxs-lookup"><span data-stu-id="32187-127">However, TAPI makes this much easier as long as the TSP itself is using a newer version than the application.</span></span> <span data-ttu-id="32187-128">Если TSP действительно новее, TAPI может перевести "вниз" в версию приложения.</span><span class="sxs-lookup"><span data-stu-id="32187-128">If the TSP is indeed newer, then TAPI is capable of translating "down" to the application's version.</span></span> <span data-ttu-id="32187-129">Например, TAPI 2,0 специалистами не обязательно должен специально поддерживать работу с TAPI версии 1,4.</span><span class="sxs-lookup"><span data-stu-id="32187-129">For example, TAPI 2.0 TSPs do not need to be specifically capable of dealing with TAPI version 1.4.</span></span> <span data-ttu-id="32187-130">Если приложение TAPI 1,4 запущено, TAPI преобразует все структуры и сообщения TAPI 2,0 в эквиваленты TAPI 1,4 или как можно ближе.</span><span class="sxs-lookup"><span data-stu-id="32187-130">If a TAPI 1.4 application is run, TAPI converts all TAPI 2.0 structures and messages into TAPI 1.4 equivalents, or as close as possible.</span></span> <span data-ttu-id="32187-131">Если в TAPI 1,4 нет близкой аппроксимации, то все сведения, относящиеся к TAPI 2,0, будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="32187-131">If there is no close approximation in TAPI 1.4, then all TAPI 2.0-specific information will be lost.</span></span>

<span data-ttu-id="32187-132">Точное значение версии расширения зависит от конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="32187-132">The precise meaning of an extension version is provider-specific.</span></span> <span data-ttu-id="32187-133">Чтобы использовать TSP, поддерживающий расширения, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="32187-133">To use a TSP that supports extensions, consult the provider's documentation.</span></span>

<span data-ttu-id="32187-134">Существует несколько версий TAPI.</span><span class="sxs-lookup"><span data-stu-id="32187-134">There are a number of versions of TAPI.</span></span> <span data-ttu-id="32187-135">Хотя большая часть этих версий включала изменения в наборы документации TAPI и интерфейс поставщика услуг телефонии (ТСПИ), существуют и другие последствия для каждой версии, а именно, различия в архитектуре, вариации операционных систем, распространяемые пакеты и проблемы при разработке TSP.</span><span class="sxs-lookup"><span data-stu-id="32187-135">While most of these versions involved changes to the TAPI and Telephony Service Provider Interface (TSPI) documentation sets, there are other implications for each version, namely, architectural differences, operating system variations, redistributables, and TSP development issues.</span></span>



| <span data-ttu-id="32187-136">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="32187-136">TAPI version</span></span>        | <span data-ttu-id="32187-137">Distribution</span><span class="sxs-lookup"><span data-stu-id="32187-137">Distribution</span></span>                                                   |
|---------------------|----------------------------------------------------------------|
| <span data-ttu-id="32187-138">1,0 – 1,2</span><span class="sxs-lookup"><span data-stu-id="32187-138">1.0 – 1.2</span></span>           | <span data-ttu-id="32187-139">Бета-версии, которые больше не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="32187-139">Beta versions that should not be used any longer.</span></span>              |
| [<span data-ttu-id="32187-140">1.4</span><span class="sxs-lookup"><span data-stu-id="32187-140">1.4</span></span>](tapi-1-4.md) | <span data-ttu-id="32187-141">Входит в Windows 95.</span><span class="sxs-lookup"><span data-stu-id="32187-141">Included in Windows 95.</span></span>                                        |
| [<span data-ttu-id="32187-142">1.5</span><span class="sxs-lookup"><span data-stu-id="32187-142">1.5</span></span>](tapi-1-5.md) | <span data-ttu-id="32187-143">Входит в Windows CE 1,0.</span><span class="sxs-lookup"><span data-stu-id="32187-143">Included in Windows CE 1.0.</span></span>                                    |
| [<span data-ttu-id="32187-144">2.0</span><span class="sxs-lookup"><span data-stu-id="32187-144">2.0</span></span>](tapi-2-0.md) | <span data-ttu-id="32187-145">Входит в состав Windows NT 4,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="32187-145">Included in Windows NT 4.0 with SP3.</span></span>                           |
| [<span data-ttu-id="32187-146">2.1</span><span class="sxs-lookup"><span data-stu-id="32187-146">2.1</span></span>](tapi-2-1.md) | <span data-ttu-id="32187-147">Входит в состав Windows NT 4,0 с пакетом обновления 4 (SP4) и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="32187-147">Included in Windows NT 4.0 with SP4 and Windows 98.</span></span>            |
| [<span data-ttu-id="32187-148">2.2</span><span class="sxs-lookup"><span data-stu-id="32187-148">2.2</span></span>](tapi-2-2.md) | <span data-ttu-id="32187-149">Входит в Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="32187-149">Included in Windows Server 2003, Windows XP, and Windows 2000.</span></span> |



 

 

 



