---
title: Справочник по индексированию ресурсов пакетов (PRI)
description: Справочник по индексированию ресурсов пакетов (PRI)
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117552"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="7617c-103">Справочник по индексированию ресурсов пакетов (PRI)</span><span class="sxs-lookup"><span data-stu-id="7617c-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="7617c-104">Набор API-интерфейсов для работы с индексатором ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7617c-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="7617c-105">Индексатор ресурсов используется для создания файлов индекса ресурсов пакета (PRI) для приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="7617c-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="7617c-106">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="7617c-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7617c-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7617c-107">In this section</span></span>

<span data-ttu-id="7617c-108">**Функции**</span><span class="sxs-lookup"><span data-stu-id="7617c-108">**Functions**</span></span>

-   <span data-ttu-id="7617c-109">Функция [**мрмкреатеконфиг**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="7617c-110">Функция [**мрмкреатеконфигинмемори**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="7617c-111">Функция [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="7617c-112">Функция [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="7617c-113">Функция [**мрмкреатересаурцеиндексер**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="7617c-114">Функция [**мрмкреатересаурцеиндексерфромпревиауспридата**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="7617c-115">Функция [**мрмкреатересаурцеиндексерфромпревиаусприфиле**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="7617c-116">Функция [**мрмкреатересаурцеиндексерфромпревиауссчемадата**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="7617c-117">Функция [**мрмкреатересаурцеиндексерфромпревиауссчемафиле**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="7617c-118">Функция [**мрмдестройиндексерандмессажес**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="7617c-119">Функция [**мрмдумпприфиле**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="7617c-120">Функция [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="7617c-121">Функция [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="7617c-122">Функция [**мрмфримемори**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="7617c-123">Функция [**мрминдексембеддеддата**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="7617c-124">Функция [**мрминдексфиле**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="7617c-125">Функция [**мрминдексфилеаутокуалифиерс**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="7617c-126">Функция [**мрминдексресаурцеконтаинераутокуалифиерс**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="7617c-127">Функция [**мрминдексстринг**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="7617c-128">Функция [**мрмпикресаурцеиндексермессажес**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="7617c-129">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="7617c-129">**Structures**</span></span>

-   <span data-ttu-id="7617c-130">Структура [**мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="7617c-131">Структура [**мрмресаурцеиндексермессаже**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="7617c-132">**Перечисления**</span><span class="sxs-lookup"><span data-stu-id="7617c-132">**Enumerations**</span></span>

-   <span data-ttu-id="7617c-133">Перечисление [**мрмдумптипе**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="7617c-134">Перечисление [**мрмпаккагингмоде**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="7617c-135">Перечисление [**мрмпаккагингоптионс**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="7617c-136">Перечисление [**мрмплатформверсион**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="7617c-137">Перечисление [**мрмресаурцеиндексермессажесеверити**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="7617c-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
