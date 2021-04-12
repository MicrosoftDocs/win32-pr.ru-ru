---
title: Обновление лицензий для магазинов, имеющих логотип Плайсфорсуре
description: Обновление лицензий для магазинов, имеющих логотип Плайсфорсуре
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Интернет-магазины проигрывателя Windows Media, обновление лицензий
- Интернет-магазины, обновление лицензий
- Интернет-магазины проигрывателя Windows Media, обновление лицензий
- Интернет-магазины, обновление лицензий
- Интернет-магазины проигрывателя Windows Media, логотип Плайсфорсуре
- Интернет-магазины, логотип Плайсфорсуре
- Обновление лицензий
- лицензии, обновление
- плайсфорсуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133523"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="3fe73-112">Обновление лицензий для магазинов, имеющих логотип Плайсфорсуре</span><span class="sxs-lookup"><span data-stu-id="3fe73-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="3fe73-113">Некоторые Интернет-Музыкальные магазины имеют логотип Плайсфорсуре, но не интегрированы с проигрывателем Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="3fe73-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="3fe73-114">Эти магазины должны предоставить документ ServiceInfo и упрощенный компонент, чтобы проигрыватель Windows Media 11 мог получать и обновлять лицензии для их содержимого.</span><span class="sxs-lookup"><span data-stu-id="3fe73-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="3fe73-115">В следующем примере показано, как работает процесс обновления лицензий.</span><span class="sxs-lookup"><span data-stu-id="3fe73-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="3fe73-116">Пользователь получает 50 музыкальных дорожек из Интернет-магазина proseware.</span><span class="sxs-lookup"><span data-stu-id="3fe73-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="3fe73-117">Каждая запись — это файл с расширением WMA.</span><span class="sxs-lookup"><span data-stu-id="3fe73-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="3fe73-118">Вместе с дорожками пользователь получает лицензии для воспроизведения дорожек.</span><span class="sxs-lookup"><span data-stu-id="3fe73-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="3fe73-119">Пользователь копирует дорожки 50 на новый компьютер с установленным проигрывателем Windows Media 11 и добавляет записи в библиотеку проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fe73-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="3fe73-120">Через некоторое время модуль обновления лицензий (ЛРМ), входящий в состав проигрывателя Windows Media 11, проверяет метаданные в 50 дорожек и определяет, что Proseware является поставщиком содержимого.</span><span class="sxs-lookup"><span data-stu-id="3fe73-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="3fe73-121">Проигрыватель Windows Media может опознать поставщик содержимого, проверив атрибут **контентдистрибутор** в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3fe73-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="3fe73-122">Если Интернет-магазин с логотипом Плайсфорсуре предоставляет файл мультимедиа, который использует Windows Media Digital Rights Management (WMDRM), Интернет-магазин должен поместить атрибут **контентдистрибутор** в файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3fe73-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="3fe73-123">Дополнительные сведения см. в разделе Добавление атрибута распространителя содержимого в пакет SDK проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fe73-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="3fe73-124">ЛРМ ищет URL-адрес документа ServiceInfo Proseware, скачивает документ и проверяет элемент **Install** документа на получение URL-адреса пакета, который лрм может использовать для установки компонента proseware.</span><span class="sxs-lookup"><span data-stu-id="3fe73-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="3fe73-125">ЛРМ устанавливает и загружает компонент.</span><span class="sxs-lookup"><span data-stu-id="3fe73-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="3fe73-126">Для каждой из 50 дорожек ЛРМ вызывает метод [ивмпсубскриптионсервице:: алловплай](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) компонента proseware.</span><span class="sxs-lookup"><span data-stu-id="3fe73-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="3fe73-127">Метод **алловплай** помещает лицензию для отдельной записи на новом компьютере и возвращает **значение true** в параметре *пфалловплай* .</span><span class="sxs-lookup"><span data-stu-id="3fe73-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="3fe73-128">Компонент Proseware должен предоставить все лицензии, необходимые для воспроизведения отдельной записи. То есть при необходимости компонент должен предоставить как корневую, так и конечную лицензию.</span><span class="sxs-lookup"><span data-stu-id="3fe73-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="3fe73-129">При первом вызове метода **алловплай** компонент Proseware должен отобразить диалоговое окно, чтобы убедиться, что текущий пользователь имеет учетную запись Proseware и имеет право на воспроизведение этой записи. При последующих вызовах **алловплай** компонент может использовать учетные данные, полученные при первом вызове, чтобы убедиться, что пользователь имеет право воспроизводить оставшиеся дорожки.</span><span class="sxs-lookup"><span data-stu-id="3fe73-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="3fe73-130">Компонент, записываемый в Интернет-магазин, должен реализовать метод **алловплай** интерфейса **ивмпсубскриптионсервице** .</span><span class="sxs-lookup"><span data-stu-id="3fe73-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="3fe73-131">Компонент должен возвращать E \_ нотимпл из каждого из трех других методов: **алловкдбурн**, **алловпдатрансфер** и **стартбаккграундпроцессинг**.</span><span class="sxs-lookup"><span data-stu-id="3fe73-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="3fe73-132">Кроме того, компонент должен присвоить параметру реестра **capabilities** значение 1; то есть \_ \_ должен быть установлен флаг возможностей алловплай подписки, и все остальные флаги возможностей должны быть сняты.</span><span class="sxs-lookup"><span data-stu-id="3fe73-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="3fe73-133">Дополнительные сведения о регистрации компонента см. в разделе [разделы реестра и записи для Интернет-магазина типа 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="3fe73-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="3fe73-134">Сведения о создании компонента, реализующего интерфейс **ивмпсубскриптионсервице** , см. в разделе [Создание подключаемого модуля для Интернет-магазина типа 2](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="3fe73-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="3fe73-135">Сведения о предоставлении корпорации Майкрософт документа ServiceInfo см. в статье отправка электронной почты группе виртуальных служб проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fe73-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="3fe73-136">Адрес электронной почты группы: mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="3fe73-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="3fe73-137">Техническое руководство по использованию различных пакетов SDK для Windows Media для создания службы, предлагающей лицензированное цифровое содержимое, можно найти в [центре разработчиков Microsoft Windows Media Center](https://msdn.microsoft.com/windowsmedia/default.aspx) и выполнить поиск по запросу "Создание Интернет-магазина Windows Media 10 с подпиской".</span><span class="sxs-lookup"><span data-stu-id="3fe73-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe73-138">См. также</span><span class="sxs-lookup"><span data-stu-id="3fe73-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe73-139">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="3fe73-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="3fe73-140">**Интернет-магазины проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3fe73-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




