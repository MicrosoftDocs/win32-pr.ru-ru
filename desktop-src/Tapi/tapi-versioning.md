---
description: Дополнительные сведения об управлении версиями для TAPI. Со временем могут быть созданы различные версии TAPI, приложений и поставщиков служб.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Управление версиями TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853cf9d5f3744e11936f121986edc4e6e027d251
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989299"
---
# <a name="tapi-versioning"></a><span data-ttu-id="395dd-104">Управление версиями TAPI</span><span class="sxs-lookup"><span data-stu-id="395dd-104">TAPI Versioning</span></span>

<span data-ttu-id="395dd-105">Со временем могут быть созданы различные версии TAPI, приложений и поставщиков служб.</span><span class="sxs-lookup"><span data-stu-id="395dd-105">Over time, different versions of TAPI, applications, and service providers may be produced.</span></span> <span data-ttu-id="395dd-106">Эти новые версии могут создавать новые определения, например для новых функций, новых элементов в структурах данных и новых битовых полей.</span><span class="sxs-lookup"><span data-stu-id="395dd-106">These new versions can make new definitions, such as for new features, new members in data structures, and new bit fields.</span></span> <span data-ttu-id="395dd-107">Следовательно, Номера версий необходимы для указания способа интерпретации различных структур данных.</span><span class="sxs-lookup"><span data-stu-id="395dd-107">Version numbers are therefore necessary to indicate how to interpret various data structures.</span></span>

<span data-ttu-id="395dd-108">Чтобы обеспечить оптимальное взаимодействие различных версий приложений, версий самой TAPI и версий поставщиков услуг разных поставщиков, Microsoft телефонии предоставляет простой механизм согласования версий для приложений.</span><span class="sxs-lookup"><span data-stu-id="395dd-108">To allow optimal interoperability of different versions of applications, versions of TAPI itself, and versions of service providers by different vendors, Microsoft Telephony provides a simple version negotiation mechanism for applications.</span></span> <span data-ttu-id="395dd-109">Существует две различные версии, которые TAPI и поставщик услуг телефонии должны согласовать для каждого устройства линии.</span><span class="sxs-lookup"><span data-stu-id="395dd-109">There are two different versions that TAPI and the telephony service provider need to agree on for each line device.</span></span> <span data-ttu-id="395dd-110">Первая — это версия, согласованная с TAPI и поставщиком услуг телефонии (TSP) Basic и дополнительная телефония, называемая версией интерфейса TAPI.</span><span class="sxs-lookup"><span data-stu-id="395dd-110">The first is the version negotiated with TAPI and the telephony service provider (TSP) Basic and Supplementary Telephony, referred to as the TAPI interface version.</span></span> <span data-ttu-id="395dd-111">Другой — для расширений, зависящих от поставщика, если таковые имеются, и называется версией расширения.</span><span class="sxs-lookup"><span data-stu-id="395dd-111">The other is for provider-specific extensions, if any, and is referred to as the extension version.</span></span> <span data-ttu-id="395dd-112">Формат структур данных и типов данных, используемых базовыми и дополнительными функциями TAPI, определяется версией TAPI, а версия расширения определяет формат структур данных, определенных расширениями, определенными для поставщика.</span><span class="sxs-lookup"><span data-stu-id="395dd-112">The format of the data structures and data types used by TAPI's Basic and Supplementary features is defined by the TAPI version, while the extension version determines the format of data structures defined by the vendor-specific extensions.</span></span>

<span data-ttu-id="395dd-113">Функция [**линенеготиатеапиверсион**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) СОГЛАСОВЫВАЕТ версию TAPI и [**линенеготиатикстверсион**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) согласовывает версию расширения TSP.</span><span class="sxs-lookup"><span data-stu-id="395dd-113">The [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) function negotiates a TAPI version and [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negotiates the TSP extension version.</span></span> <span data-ttu-id="395dd-114">Один TSP может обрабатывать более одной версии, и приложение должно "возвращаться" к использованию более старой версии, если используется более старая версия TSP.</span><span class="sxs-lookup"><span data-stu-id="395dd-114">A single TSP could be capable of handling more than one version, and an application must "fall back" to using an older version if using an older TSP.</span></span> <span data-ttu-id="395dd-115">В **линенеготиатеапиверсион** параметр *двапиверсион* по умолчанию имеет значение в соответствии с версией, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="395dd-115">In **lineNegotiateAPIVersion** the *dwApiVersion* parameter defaults to a value according to version, as follows.</span></span>



| <span data-ttu-id="395dd-116">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="395dd-116">TAPI version</span></span> | <span data-ttu-id="395dd-117">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="395dd-117">Default value</span></span> |
|--------------|---------------|
| <span data-ttu-id="395dd-118">1,3</span><span class="sxs-lookup"><span data-stu-id="395dd-118">1.3</span></span>          | <span data-ttu-id="395dd-119">0x00010003</span><span class="sxs-lookup"><span data-stu-id="395dd-119">0x00010003</span></span>    |
| <span data-ttu-id="395dd-120">1.4</span><span class="sxs-lookup"><span data-stu-id="395dd-120">1.4</span></span>          | <span data-ttu-id="395dd-121">0x00010004</span><span class="sxs-lookup"><span data-stu-id="395dd-121">0x00010004</span></span>    |
| <span data-ttu-id="395dd-122">2.0</span><span class="sxs-lookup"><span data-stu-id="395dd-122">2.0</span></span>          | <span data-ttu-id="395dd-123">0x00020000</span><span class="sxs-lookup"><span data-stu-id="395dd-123">0x00020000</span></span>    |
| <span data-ttu-id="395dd-124">2.1</span><span class="sxs-lookup"><span data-stu-id="395dd-124">2.1</span></span>          | <span data-ttu-id="395dd-125">0x00020001</span><span class="sxs-lookup"><span data-stu-id="395dd-125">0x00020001</span></span>    |
| <span data-ttu-id="395dd-126">2.2</span><span class="sxs-lookup"><span data-stu-id="395dd-126">2.2</span></span>          | <span data-ttu-id="395dd-127">0x00020002</span><span class="sxs-lookup"><span data-stu-id="395dd-127">0x00020002</span></span>    |



 

<span data-ttu-id="395dd-128">Тем не менее TAPI делает это гораздо проще, если сам TSP использует более новую версию, чем приложение.</span><span class="sxs-lookup"><span data-stu-id="395dd-128">However, TAPI makes this much easier as long as the TSP itself is using a newer version than the application.</span></span> <span data-ttu-id="395dd-129">Если TSP действительно новее, TAPI может перевести "вниз" в версию приложения.</span><span class="sxs-lookup"><span data-stu-id="395dd-129">If the TSP is indeed newer, then TAPI is capable of translating "down" to the application's version.</span></span> <span data-ttu-id="395dd-130">Например, TAPI 2,0 специалистами не обязательно должен специально поддерживать работу с TAPI версии 1,4.</span><span class="sxs-lookup"><span data-stu-id="395dd-130">For example, TAPI 2.0 TSPs do not need to be specifically capable of dealing with TAPI version 1.4.</span></span> <span data-ttu-id="395dd-131">Если приложение TAPI 1,4 запущено, TAPI преобразует все структуры и сообщения TAPI 2,0 в эквиваленты TAPI 1,4 или как можно ближе.</span><span class="sxs-lookup"><span data-stu-id="395dd-131">If a TAPI 1.4 application is run, TAPI converts all TAPI 2.0 structures and messages into TAPI 1.4 equivalents, or as close as possible.</span></span> <span data-ttu-id="395dd-132">Если в TAPI 1,4 нет близкой аппроксимации, то все сведения, относящиеся к TAPI 2,0, будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="395dd-132">If there is no close approximation in TAPI 1.4, then all TAPI 2.0-specific information will be lost.</span></span>

<span data-ttu-id="395dd-133">Точное значение версии расширения зависит от конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="395dd-133">The precise meaning of an extension version is provider-specific.</span></span> <span data-ttu-id="395dd-134">Чтобы использовать TSP, поддерживающий расширения, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="395dd-134">To use a TSP that supports extensions, consult the provider's documentation.</span></span>

<span data-ttu-id="395dd-135">Существует несколько версий TAPI.</span><span class="sxs-lookup"><span data-stu-id="395dd-135">There are a number of versions of TAPI.</span></span> <span data-ttu-id="395dd-136">Хотя большая часть этих версий включала изменения в наборы документации TAPI и интерфейс поставщика услуг телефонии (ТСПИ), существуют и другие последствия для каждой версии, а именно, различия в архитектуре, вариации операционных систем, распространяемые пакеты и проблемы при разработке TSP.</span><span class="sxs-lookup"><span data-stu-id="395dd-136">While most of these versions involved changes to the TAPI and Telephony Service Provider Interface (TSPI) documentation sets, there are other implications for each version, namely, architectural differences, operating system variations, redistributables, and TSP development issues.</span></span>



| <span data-ttu-id="395dd-137">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="395dd-137">TAPI version</span></span>        | <span data-ttu-id="395dd-138">Distribution</span><span class="sxs-lookup"><span data-stu-id="395dd-138">Distribution</span></span>                                                   |
|---------------------|----------------------------------------------------------------|
| <span data-ttu-id="395dd-139">1,0 – 1,2</span><span class="sxs-lookup"><span data-stu-id="395dd-139">1.0 – 1.2</span></span>           | <span data-ttu-id="395dd-140">Бета-версии, которые больше не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="395dd-140">Beta versions that should not be used any longer.</span></span>              |
| [<span data-ttu-id="395dd-141">1.4</span><span class="sxs-lookup"><span data-stu-id="395dd-141">1.4</span></span>](tapi-1-4.md) | <span data-ttu-id="395dd-142">Входит в Windows 95.</span><span class="sxs-lookup"><span data-stu-id="395dd-142">Included in Windows 95.</span></span>                                        |
| [<span data-ttu-id="395dd-143">1.5</span><span class="sxs-lookup"><span data-stu-id="395dd-143">1.5</span></span>](tapi-1-5.md) | <span data-ttu-id="395dd-144">Входит в Windows CE 1,0.</span><span class="sxs-lookup"><span data-stu-id="395dd-144">Included in Windows CE 1.0.</span></span>                                    |
| [<span data-ttu-id="395dd-145">2.0</span><span class="sxs-lookup"><span data-stu-id="395dd-145">2.0</span></span>](tapi-2-0.md) | <span data-ttu-id="395dd-146">Входит в состав Windows NT 4,0 с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="395dd-146">Included in Windows NT 4.0 with SP3.</span></span>                           |
| [<span data-ttu-id="395dd-147">2.1</span><span class="sxs-lookup"><span data-stu-id="395dd-147">2.1</span></span>](tapi-2-1.md) | <span data-ttu-id="395dd-148">Входит в состав Windows NT 4,0 с пакетом обновления 4 (SP4) и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="395dd-148">Included in Windows NT 4.0 with SP4 and Windows 98.</span></span>            |
| [<span data-ttu-id="395dd-149">2.2</span><span class="sxs-lookup"><span data-stu-id="395dd-149">2.2</span></span>](tapi-2-2.md) | <span data-ttu-id="395dd-150">Входит в Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="395dd-150">Included in Windows Server 2003, Windows XP, and Windows 2000.</span></span> |



 

 

 



