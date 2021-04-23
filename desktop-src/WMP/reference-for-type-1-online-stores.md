---
title: Справочные материалы по интернет-магазинам типа 1
description: Справочные материалы по интернет-магазинам типа 1
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Интернет-магазины проигрывателя Windows Media, справочные материалы
- Интернет-магазины, справочные материалы
- Тип 1 Интернет-магазины, справочные материалы
- Справочник по Интернет-магазинам типа 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412694"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="b978d-107">Справочные материалы по интернет-магазинам типа 1</span><span class="sxs-lookup"><span data-stu-id="b978d-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="b978d-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="b978d-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b978d-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b978d-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b978d-110">Проигрыватель Windows Media 11 предоставляет компилятор каталога, объект и несколько интерфейсов, поддерживающих Интернет-магазины типа 1.</span><span class="sxs-lookup"><span data-stu-id="b978d-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="b978d-111">Эти сведения подробно описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b978d-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="b978d-112">Section</span><span class="sxs-lookup"><span data-stu-id="b978d-112">Section</span></span>                                                                                    | <span data-ttu-id="b978d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b978d-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b978d-114">Компилятор каталога для Интернет-магазинов типа 1</span><span class="sxs-lookup"><span data-stu-id="b978d-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="b978d-115">Содержит справочные материалы по компилятору, используемому Интернет-магазином для компиляции музыкального каталога.</span><span class="sxs-lookup"><span data-stu-id="b978d-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="b978d-116">Интерфейс Ивмпконтентконтаинер</span><span class="sxs-lookup"><span data-stu-id="b978d-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="b978d-117">Содержит справочные страницы для методов, которые вызывает подключаемый модуль интернет-магазина для проверки контейнера содержимого.</span><span class="sxs-lookup"><span data-stu-id="b978d-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="b978d-118">Контейнер содержимого представляет собой набор элементов мультимедиа для скачивания или покупки.</span><span class="sxs-lookup"><span data-stu-id="b978d-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="b978d-119">Реализовано проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b978d-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="b978d-120">Интерфейс Ивмпконтентконтаинерлист</span><span class="sxs-lookup"><span data-stu-id="b978d-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="b978d-121">Содержит справочные страницы для методов, которые вызывает подключаемый модуль интернет-магазина для проверки списка контейнеров содержимого.</span><span class="sxs-lookup"><span data-stu-id="b978d-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="b978d-122">Реализовано проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b978d-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="b978d-123">Интерфейс Ивмпконтентпартнер</span><span class="sxs-lookup"><span data-stu-id="b978d-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="b978d-124">Содержит справочные страницы по методам, которые вызываются проигрывателем Windows Media для получения информации из Интернет-магазина и уведомления Интернет-магазина о действиях пользователя.</span><span class="sxs-lookup"><span data-stu-id="b978d-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="b978d-125">Реализуется подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="b978d-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="b978d-126">Интерфейс Ивмпконтентпартнеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="b978d-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="b978d-127">Содержит справочные страницы для методов, которые вызывает подключаемый модуль интернет-магазина для уведомления проигрывателя Windows Media о завершении асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="b978d-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="b978d-128">Реализовано проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b978d-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="b978d-129">Внешний объект для Интернет-магазинов типа 1</span><span class="sxs-lookup"><span data-stu-id="b978d-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="b978d-130">Содержит справочные страницы по свойствам, методам и событиям, используемым скриптом на веб-страницах, предоставляемых Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="b978d-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="b978d-131">Перечисления для Интернет-магазинов типа 1</span><span class="sxs-lookup"><span data-stu-id="b978d-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="b978d-132">Содержит справочные страницы для перечислений, используемых при обмене данными между проигрывателем Windows Media и подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="b978d-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="b978d-133">Структуры для Интернет-магазинов типа 1</span><span class="sxs-lookup"><span data-stu-id="b978d-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="b978d-134">Содержит справочные страницы по структурам, используемым при обмене данными между проигрывателем Windows Media и подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="b978d-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="b978d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b978d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b978d-136">**Тип 1 Интернет-магазины**</span><span class="sxs-lookup"><span data-stu-id="b978d-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




