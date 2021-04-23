---
title: ЛОГУРЛ, элемент
description: Элемент ЛОГУРЛ указывает проигрывателю Windows Media отправлять любые данные журнала по указанному URL-адресу.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Проигрыватель Windows Media, элемент ЛОГУРЛ
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704412"
---
# <a name="logurl-element"></a><span data-ttu-id="fd275-104">ЛОГУРЛ, элемент</span><span class="sxs-lookup"><span data-stu-id="fd275-104">LOGURL Element</span></span>

<span data-ttu-id="fd275-105">Элемент **логурл** указывает проигрывателю Windows Media отправлять любые данные журнала по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="fd275-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="fd275-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fd275-106">Attributes</span></span>

<span data-ttu-id="fd275-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="fd275-107">**HREF** (required)</span></span>

<span data-ttu-id="fd275-108">URL-адрес узла, который может обрабатывать запросы на ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="fd275-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fd275-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fd275-109">Parent/Child Elements</span></span>



| <span data-ttu-id="fd275-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="fd275-110">Hierarchy</span></span>       | <span data-ttu-id="fd275-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="fd275-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="fd275-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fd275-112">Parent elements</span></span> | <span data-ttu-id="fd275-113">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="fd275-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="fd275-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fd275-114">Child elements</span></span>  | <span data-ttu-id="fd275-115">Нет</span><span class="sxs-lookup"><span data-stu-id="fd275-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="fd275-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd275-116">Remarks</span></span>

<span data-ttu-id="fd275-117">Элемент **логурл** позволяет списку воспроизведения клиентского метафайла отправить дополнительные сведения о ведении журнала на указанные серверы.</span><span class="sxs-lookup"><span data-stu-id="fd275-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="fd275-118">Данные журнала автоматически отправляются на сервер-источник списка воспроизведения при его открытии и для каждого **логурл** , указанного для элемента **ASX** , если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="fd275-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="fd275-119">Сведения о ведении журнала также отправляются в каждый **логурл** , указанный для элемента **entry** при достижении этой записи.</span><span class="sxs-lookup"><span data-stu-id="fd275-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="fd275-120">URL-адрес, указанный в атрибуте **href** элемента **логурл** , должен быть адресом узла, который может обрабатывать запросы на ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="fd275-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="fd275-121">URL-адрес может быть любым допустимым URL-адресом HTTP.</span><span class="sxs-lookup"><span data-stu-id="fd275-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="fd275-122">URL-адрес также может указывать расположение сценария CGI.</span><span class="sxs-lookup"><span data-stu-id="fd275-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="fd275-123">Единственными допустимыми протоколами для элемента **логурл** являются HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fd275-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="fd275-124">Элемент **логурл** внутри области элемента **ASX** применим только к метафайлу, в котором он находится, независимо от того, есть ли ссылка на этот метафайл из другого метафайла.</span><span class="sxs-lookup"><span data-stu-id="fd275-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="fd275-125">Элемент **логурл** вызывает принудительную отправку данных журнала для всего потока содержимого из заданной области и только для потока содержимого из его заданной области.</span><span class="sxs-lookup"><span data-stu-id="fd275-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="fd275-126">Данные журнала будут отправлены на сервер-источник и все URL-адреса, перечисленные в каждом элементе **логурл** в области.</span><span class="sxs-lookup"><span data-stu-id="fd275-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="fd275-127">Данные журнала будут отправляться только один раз на каждый указанный URL-адрес, даже если один и тот же URL-адрес указан более одного раза в заданной области.</span><span class="sxs-lookup"><span data-stu-id="fd275-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="fd275-128">Повтор **записи** приведет к другой отправке в указанные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="fd275-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="fd275-129">Число элементов **логурл** в списке воспроизведения метафайлов не ограничено.</span><span class="sxs-lookup"><span data-stu-id="fd275-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="fd275-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd275-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="fd275-131">Ниже приведены примеры допустимых URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="fd275-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="fd275-132">URL-адрес приложения ISAPI:</span><span class="sxs-lookup"><span data-stu-id="fd275-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="fd275-133">URL-адрес скрипта CGI:</span><span class="sxs-lookup"><span data-stu-id="fd275-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="fd275-134">Допустимый URL-адрес HTTP:</span><span class="sxs-lookup"><span data-stu-id="fd275-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="fd275-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fd275-135">Requirements</span></span>



| <span data-ttu-id="fd275-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fd275-136">Requirement</span></span> | <span data-ttu-id="fd275-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fd275-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="fd275-138">Версия</span><span class="sxs-lookup"><span data-stu-id="fd275-138">Version</span></span><br/> | <span data-ttu-id="fd275-139">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="fd275-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd275-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd275-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd275-141">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fd275-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="fd275-142">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fd275-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





