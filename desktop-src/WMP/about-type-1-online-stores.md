---
title: Сведения об Интернет-магазинах типа 1
description: Сведения об Интернет-магазинах типа 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Интернет-магазины проигрывателя Windows Media, введите 1 Интернет-магазины
- Интернет-магазины, тип 1 Интернет-магазины
- Тип 1 Интернет-магазины, сведения
- Проигрыватель Windows Media, введите 1 Интернет-магазины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691462"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="68610-107">Сведения об Интернет-магазинах типа 1</span><span class="sxs-lookup"><span data-stu-id="68610-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="68610-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="68610-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="68610-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="68610-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="68610-110">Проигрыватель Microsoft Windows Media 11 поддерживает два типа Интернет-магазинов: тип 1 и тип 2.</span><span class="sxs-lookup"><span data-stu-id="68610-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="68610-111">Хранилища типа 1 более тесно интегрированы в проигрывателе Windows Media, чем типы магазинов типа 2.</span><span class="sxs-lookup"><span data-stu-id="68610-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="68610-112">Интернет-магазин типа 1 предоставляет загружаемый каталог музыки, чтобы проигрыватель Windows Media мог предоставить пользователю доступ к содержимому магазина, как если бы содержимое находилось в локальной библиотеке мультимедиа пользователя.</span><span class="sxs-lookup"><span data-stu-id="68610-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="68610-113">Интернет-магазин типа 1 должен предоставлять подключаемый модуль, реализующий интерфейс [ивмпконтентпартнер](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="68610-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="68610-114">Когда пользователь переходит в пользовательский интерфейс проигрывателя Windows Media, проигрыватель вызывает подключаемый модуль, чтобы Интернет-магазин мог улучшить взаимодействие с пользователем, предоставляя веб-страницы, отображаемые в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="68610-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="68610-115">Возможности Интернет-магазинов типа 1, которые отличают их от магазинов типа 2, включают следующее:</span><span class="sxs-lookup"><span data-stu-id="68610-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="68610-116">**Простота использования.**</span><span class="sxs-lookup"><span data-stu-id="68610-116">**Ease of use.**</span></span> <span data-ttu-id="68610-117">Пользователи могут просматривать музыку из каталога Интернет-магазина, используя тот же привычный пользовательский интерфейс проигрывателя Windows Media, который в настоящее время используется для управления личной библиотекой.</span><span class="sxs-lookup"><span data-stu-id="68610-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="68610-118">Пользователи могут просматривать только один каталог Интернет-магазина в функции просмотра в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="68610-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="68610-119">**Удобным.**</span><span class="sxs-lookup"><span data-stu-id="68610-119">**Convenience.**</span></span> <span data-ttu-id="68610-120">Пользователи могут выполнять выборку или приобретение музыки, не переходя от функции просмотра к другой части пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="68610-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="68610-121">**Широкие возможности.**</span><span class="sxs-lookup"><span data-stu-id="68610-121">**Rich features.**</span></span> <span data-ttu-id="68610-122">Так как каталог Интернет-магазина хранится аналогично библиотеке пользователя, многие функции библиотеки проигрывателя Windows Media могут быть применены к каталогу.</span><span class="sxs-lookup"><span data-stu-id="68610-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="68610-123">Например, пользователи могут использовать для фильтрации каталога Интернет-магазина слово «Обзор».</span><span class="sxs-lookup"><span data-stu-id="68610-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="68610-124">Для поставщика Интернет-магазина преимущества предоставления хранилища типа 1, а не хранилища типа 2 включают следующее.</span><span class="sxs-lookup"><span data-stu-id="68610-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="68610-125">Пользовательский узел с высокой видимостью в дереве библиотеки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="68610-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="68610-126">Система, предназначенная для покупок музыки.</span><span class="sxs-lookup"><span data-stu-id="68610-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="68610-127">Улучшенные подключения к процессам проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="68610-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="68610-128">Более удобный и простой в использовании диспетчер загрузки.</span><span class="sxs-lookup"><span data-stu-id="68610-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="68610-129">Возможность перехода между различными функциями проигрывателя (включая открытие определенных узлов дерева библиотеки).</span><span class="sxs-lookup"><span data-stu-id="68610-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="68610-130">Уведомления об истечении срока действия лицензии для содержимого подписки.</span><span class="sxs-lookup"><span data-stu-id="68610-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="68610-131">Уведомления для работы с подключенными портативными музыкальными проигрывателями.</span><span class="sxs-lookup"><span data-stu-id="68610-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="68610-132">В следующих разделах содержатся общие сведения об Интернет-магазинах типа 1.</span><span class="sxs-lookup"><span data-stu-id="68610-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="68610-133">Section</span><span class="sxs-lookup"><span data-stu-id="68610-133">Section</span></span>                                                                                              | <span data-ttu-id="68610-134">Описание</span><span class="sxs-lookup"><span data-stu-id="68610-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68610-135">Каталог музыки</span><span class="sxs-lookup"><span data-stu-id="68610-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="68610-136">Описание каталога музыки, предоставляемого Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="68610-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="68610-137">Описывает компилятор каталога, предоставляемый корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="68610-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="68610-138">Контейнеры содержимого</span><span class="sxs-lookup"><span data-stu-id="68610-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="68610-139">Описывает интерфейс контейнера содержимого ([ивмпконтентконтаинер](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), который используется для представления коллекции элементов мультимедиа для покупки или загрузки.</span><span class="sxs-lookup"><span data-stu-id="68610-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="68610-140">Интеграция библиотеки</span><span class="sxs-lookup"><span data-stu-id="68610-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="68610-141">Описывает, как каталог музыкального хранилища в Интернет-магазине интегрируется в представление библиотеки проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="68610-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="68610-142">Страницы обнаружения</span><span class="sxs-lookup"><span data-stu-id="68610-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="68610-143">Описание взаимодействия проигрывателя Windows Media и веб-страниц, предоставляемых Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="68610-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="68610-144">Контекстные меню</span><span class="sxs-lookup"><span data-stu-id="68610-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="68610-145">Описывает, как Интернет-магазин может предоставлять контекстные меню при переходе пользователя по интерфейсу проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="68610-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="68610-146">Звуковые потоки</span><span class="sxs-lookup"><span data-stu-id="68610-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="68610-147">Описание того, как Интернет-магазин предоставляет проигрыватель Windows Media с URL-адресом для потоковой передачи аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="68610-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="68610-148">Документ ServiceInfo для Интернет-магазина типа 1</span><span class="sxs-lookup"><span data-stu-id="68610-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="68610-149">Описывает XML-документ ServiceInfo, предоставленный Интернет-магазином типа 1.</span><span class="sxs-lookup"><span data-stu-id="68610-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="68610-150">Тип 1 подключаемый модуль интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="68610-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="68610-151">Описывает подключаемый модуль, который должен предоставлять Интернет-магазин типа 1.</span><span class="sxs-lookup"><span data-stu-id="68610-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="68610-152">См. также</span><span class="sxs-lookup"><span data-stu-id="68610-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68610-153">**Тип 1 Интернет-магазины**</span><span class="sxs-lookup"><span data-stu-id="68610-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




