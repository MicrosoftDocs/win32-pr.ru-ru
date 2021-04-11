---
title: Ведение журнала данных потока
description: Ведение журнала данных потока
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Списки воспроизведения метафайлов Windows Media, ведение журнала данных потока
- списки воспроизведения, ведение журнала данных потока
- списки воспроизведения метафайлов, ведение журнала данных потока
- Списки воспроизведения метафайлов Windows Media, ведение журнала потоковых данных
- списки воспроизведения, ведение журнала потоковых данных
- списки воспроизведения метафайлов, ведение журнала потоковых данных
- ведение журнала данных потока
- ведение журнала потоковых данных
- Проигрыватель Windows Media, запись данных потока в журнал
- Проигрыватель Windows Media, ведение журнала потоковых данных
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133046"
---
# <a name="logging-stream-data"></a><span data-ttu-id="59aec-113">Ведение журнала данных потока</span><span class="sxs-lookup"><span data-stu-id="59aec-113">Logging Stream Data</span></span>

<span data-ttu-id="59aec-114">Записанные в журнал данные могут быть получены и использованы для определения поведения средства просмотра, например частоту просмотра потока или просмотра пользователем потока, а также времени, в течение которого пользователь просматривал поток и в течение определенного качества.</span><span class="sxs-lookup"><span data-stu-id="59aec-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="59aec-115">Данные журнала автоматически отправляются на сервер, с которого был создан список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="59aec-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="59aec-116">Можно также отправить данные журнала на дополнительные серверы, включая веб-серверы, которые используются исключительно для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="59aec-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="59aec-117">Для этого используйте элемент **логурл** , указав допустимый URL-адрес для атрибута **href** .</span><span class="sxs-lookup"><span data-stu-id="59aec-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="59aec-118">Элементы **логурл** можно включать в качестве дочерних элементов для элемента **ASX** и как дочерние элементы отдельных элементов **записи** .</span><span class="sxs-lookup"><span data-stu-id="59aec-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="59aec-119">При первом открытии списка воспроизведения данные журнала отправляются на сервер-источник и каждый URL-адрес, указанный в **логурл** потомков элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="59aec-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="59aec-120">Затем при достижении каждой записи данные, относящиеся к этой записи, отправляются каждому URL-адресу, указанному в **логурл** потомков элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="59aec-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="59aec-121">Пакет SDK Windows Media Format поддерживает элемент **логурл** через интерфейс **ивмсреадернетворкконфиг** и следующие методы:</span><span class="sxs-lookup"><span data-stu-id="59aec-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="59aec-122">В дополнение к сведениям, которые регистрируются автоматически, список воспроизведения метафайлов может регистрировать пользовательскую информацию с помощью элемента **param** .</span><span class="sxs-lookup"><span data-stu-id="59aec-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="59aec-123">Чтобы использовать элемент **param** таким образом, задайте для атрибута **Name** значение "log:", за которым следует имя поля журнала, а также необязательное пространство имен XML, отделенное от имени поля другим двоеточием (":").</span><span class="sxs-lookup"><span data-stu-id="59aec-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="59aec-124">Все после второго двоеточия рассматривается как пространство имен, поэтому имя поля не должно содержать двоеточие.</span><span class="sxs-lookup"><span data-stu-id="59aec-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="59aec-125">В поле журнала, указанном в атрибуте **Name** , задается значение атрибута **value** .</span><span class="sxs-lookup"><span data-stu-id="59aec-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="59aec-126">Если журнал еще не содержит поле с указанным именем, оно будет добавлено.</span><span class="sxs-lookup"><span data-stu-id="59aec-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="59aec-127">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="59aec-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="59aec-128">См. также</span><span class="sxs-lookup"><span data-stu-id="59aec-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59aec-129">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="59aec-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="59aec-130">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="59aec-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




