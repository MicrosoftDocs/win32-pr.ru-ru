---
title: Загрузка мультимедийного содержимого
description: Загрузка мультимедийного содержимого
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Интернет-магазины проигрывателя Windows Media, Загрузка мультимедийного содержимого
- Интернет-магазины, Загрузка мультимедийного содержимого
- Тип 1 Интернет-магазины, Загрузка мультимедийного содержимого
- Интернет-магазины проигрывателя Windows Media, Загрузка содержимого мультимедиа
- Интернет-магазины, Загрузка содержимого мультимедиа
- Тип 1 Интернет-магазины, скачивание содержимого мультимедиа
- мультимедийное содержимое, скачивание
- Загрузка мультимедийного содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104412687"
---
# <a name="downloading-media-content"></a><span data-ttu-id="c8bb7-111">Загрузка мультимедийного содержимого</span><span class="sxs-lookup"><span data-stu-id="c8bb7-111">Downloading Media Content</span></span>

<span data-ttu-id="c8bb7-112">Проигрыватель Windows Media обрабатывает файлы для скачивания музыкальных файлов в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="c8bb7-113">Загрузка может быть инициирована, когда страница обнаружения вызывает [внешнюю. download](external-download.md) или когда пользователь выбирает, в проигрывателе, чтобы скачать набор дорожек.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="c8bb7-114">В любом случае проигрыватель Windows Media вызывает [ивмпконтентпартнер::D гружать](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), передавая список контейнеров содержимого, описывающий набор загружаемых дорожек, и файл cookie, представляющий транзакцию загрузки.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="c8bb7-115">Затем подключаемый модуль партнера по содержимому должен вызвать [ивмпконтентпартнеркаллбакк::D овнлоадтракк](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) один раз для каждой записи в наборе.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="c8bb7-116">Когда подключаемый модуль вызывает **довнлоадтракк**, он передает **значение HRESULT** в параметре *хрдовнлоад* .</span><span class="sxs-lookup"><span data-stu-id="c8bb7-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="c8bb7-117">Если подключаемый модуль передает код успешного выполнения в *хрдовнлоад*, проигрыватель Windows Media загружает эту запись. Если подключаемый модуль передает код ошибки в *хрдовнлоад*, проигрыватель не скачивает эту запись. Для каждого вызова для **загрузки** подключаемый модуль должен предоставить файл cookie транзакции и идентификатор рассматриваемой записи.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="c8bb7-118">Для дорожек, которые будут загружены, подключаемый модуль также должен предоставить URL-адрес дорожки.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="c8bb7-119">После загрузки файла проигрыватель Windows Media автоматически обновляет библиотеку, чтобы отразить только что приобретенную музыку.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="c8bb7-120">Проигрыватель предоставляет сведения о состоянии подключаемому модулю для операции загрузки путем вызова [ивмпконтентпартнер::D овнлоадтракккомплете](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span><span class="sxs-lookup"><span data-stu-id="c8bb7-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="c8bb7-121">В этом методе проигрыватель предоставляет **HRESULT** для указания на успешность или сбой скачивания, идентификатор записи и строку настраиваемых параметров, предоставленную Интернет-магазином при вызове **довнлоадтракк**.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8bb7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c8bb7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8bb7-123">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="c8bb7-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




