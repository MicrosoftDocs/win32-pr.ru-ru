---
title: Настройка доставки мультимедиа
description: Настройка доставки мультимедиа
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Списки воспроизведения метафайлов Windows Media, Настройка доставки мультимедиа
- списки воспроизведения, Настройка доставки мультимедиа
- списки воспроизведения метафайлов, Настройка доставки мультимедиа
- Списки воспроизведения метафайлов Windows Media, персонализация доставки мультимедиа
- списки воспроизведения, персонализация доставки мультимедиа
- списки воспроизведения метафайлов, персонализация доставки мультимедиа
- Персонализация доставки мультимедиа
- Настройка доставки мультимедиа
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252861"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="4c4e6-111">Настройка доставки мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4c4e6-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="4c4e6-112">В отличие от односторонней связи, которая передает идентичное содержимое массовой аудитории, технологии Windows Media предоставляют средства для использования демографических данных, индивидуализируйте широковещательные рассылки.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="4c4e6-113">Благодаря Интернету двусторонняя связь в крупном масштабе доступна.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="4c4e6-114">Этот динамический обмен информацией позволяет поставщикам содержимого узнавать свою аудиторию и реагировать на настроенные презентации.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="4c4e6-115">В следующем примере с помощью вымышленной компании показано, как можно персонализировать потоковую передачу содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="4c4e6-116">В этом обсуждении предполагается, что вы знакомы с Active Server страницами (ASP или файлы ASP) и определением переменных.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="4c4e6-117">«Новости» — это вымышленная организация с новостями, которая развернула свои операции для включения веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="4c4e6-118">Основной компонент сайта — это раздел, в котором пользователи могут создавать собственные персонализированные невскастс.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="4c4e6-119">Вместо того чтобы просматривать традиционные невскаст, предназначенные для массовой аудитории, пользователь видит полную программу новостей, которая содержит только темы личного интереса.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="4c4e6-120">Следующая последовательность описывает типичное взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="4c4e6-121">Новый пользователь переходит на сайт и нажимает кнопку **создать личный невскаст**.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="4c4e6-122">Откроется форма предпочтений.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-122">A preference form opens.</span></span> <span data-ttu-id="4c4e6-123">В этой форме пользователь отвечает на вопросы о личных предпочтениях, например о избранных новостях, наименее избранных новостях, хобби и обычном способе получения ежедневных новостей.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="4c4e6-124">Пользователь отправляет эти сведения, и через несколько секунд вы просматриваете полный, 15-минутный, персональный невскаст, содержащий содержимое программы, переходы и коммерческие приложения.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="4c4e6-125">Выбор каждого элемента мультимедиа, включая коммерческие, зависит от профиля пользователя и выполняется автоматически с компонентами технологий Windows Media и готовыми Интернет-инструментами.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="4c4e6-126">В следующем списке описано, как различные средства взаимодействуют для создания персонализированной невскаст.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="4c4e6-127">Форма предпочтения, заполняемая пользователем, — это страница Active Server (ASP) (Choice. ASP).</span><span class="sxs-lookup"><span data-stu-id="4c4e6-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="4c4e6-128">Данные, полученные из формы предпочтений, анализируются двумя серверными компонентами.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="4c4e6-129">Один компонент использует эти сведения для запроса Microsoft SQL Server базы данных новостей.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="4c4e6-130">Другой компонент — это сервер AD, использующий сложные наборы правил, основанные на контрактных требованиях и демографических данных, чтобы запланировать в это время рекламу, соответствующую пользователю.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="4c4e6-131">Две базы данных возвращают различные части списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="4c4e6-132">База данных новостей о новостях возвращает набор соответствующих записей истории, а сервер AD возвращает набор соответствующих коммерческих записей.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="4c4e6-133">Вторая ASP-страница (Плайшов. ASP) получает записи из базы данных новостей и сервера AD и объединяет их со стандартными записями Open, Close и Transition.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="4c4e6-134">Все записи затем размещаются в соответствии с шаблоном, предоставленным Плайшов. ASP, и страница ASP возвращает список воспроизведения пользователю.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="4c4e6-135">Встроенный элемент управления проигрывателя Windows Media на компьютере пользователя воспроизводит список воспроизведения от начала до конца, и пользователь просматривает персонализированную невскаст.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="4c4e6-136">В следующем примере показана часть файла списка воспроизведения, который может получить пользователь.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="4c4e6-137">В нее добавлены баннеры, ссылки МОРЕИНФО и АБСТРАКЦИи.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="4c4e6-138">Названия организаций, предприятий и изделий, а также имена и события, используемые в качестве примеров, являются вымышленными.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="4c4e6-139">Возможное сходство с реально существующими организациями, предприятиями, изделиями, лицами и событиями следует рассматривать как случайное.</span><span class="sxs-lookup"><span data-stu-id="4c4e6-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c4e6-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4c4e6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c4e6-141">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="4c4e6-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4c4e6-142">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="4c4e6-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4c4e6-143">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="4c4e6-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4c4e6-144">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4c4e6-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4c4e6-145">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4c4e6-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




