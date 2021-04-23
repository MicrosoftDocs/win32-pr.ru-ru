---
title: Элемент Reference (не рекомендуется)
description: Элемент Reference (не рекомендуется)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Метафайлы Windows Media, элемент Reference
- Метафайлы, ссылочный элемент
- Reference, элемент
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700622"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="83ce5-106">Элемент Reference (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="83ce5-106">reference Element (deprecated)</span></span>

<span data-ttu-id="83ce5-107">В этом разделе документируется функция, которая больше не используется в текущей версии метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83ce5-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="83ce5-108">Элемент **Reference** содержит список ссылок на URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="83ce5-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="83ce5-109">Каждый элемент в списке имеет   =  *URL-адрес* ref XX, где *XX* — целое число, а *URL* — URL-адрес файла ASF.</span><span class="sxs-lookup"><span data-stu-id="83ce5-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="83ce5-110">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="83ce5-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="83ce5-111">Целые числа, представленные значением *XX* , должны быть в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="83ce5-112">То есть целое число в каждой строке должно быть больше, чем целое число в предыдущей строке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="83ce5-113">Когда клиентская программа считывает элемент Reference, он пытается подключиться к файлу мультимедиа, представленному первым URL-адресом в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="83ce5-114">Если это не удается, клиентская программа пытается подключиться к файлу, представленному следующим URL-адресом в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="83ce5-115">Клиентская программа переходит в список до тех пор, пока не будет выполнено успешное подключение или не достигнет конца списка.</span><span class="sxs-lookup"><span data-stu-id="83ce5-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="83ce5-116">Обратите внимание, что если клиентская программа устанавливает успешное подключение, она не считывает ни одного из последующих URL-адресов в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="83ce5-117">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="83ce5-117">**Example Code**</span></span>

<span data-ttu-id="83ce5-118">В следующем примере клиентская программа сначала пытается подключиться к файлу, представленному URL-адресом MMS.</span><span class="sxs-lookup"><span data-stu-id="83ce5-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="83ce5-119">Если это не удалось, клиентская программа попытается подключиться к файлу, представленному URL-адресом HTTP.</span><span class="sxs-lookup"><span data-stu-id="83ce5-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="83ce5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83ce5-120">Remarks</span></span>

<span data-ttu-id="83ce5-121">Формат файлов ASF включает в себя разнообразные типы мультимедиа, включая аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="83ce5-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="83ce5-122">Файлы ASF также используют несколько расширений имен файлов, включая файлы WMA и WMV.</span><span class="sxs-lookup"><span data-stu-id="83ce5-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="83ce5-123">Целые числа, представленные значением *XX* , должны быть в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="83ce5-124">То есть целое число в каждой строке должно быть больше, чем целое число в предыдущей строке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="83ce5-125">Когда клиентская программа считывает элемент Reference, он пытается подключиться к файлу мультимедиа, представленному первым URL-адресом в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="83ce5-126">Если это не удается, клиентская программа пытается подключиться к файлу, представленному следующим URL-адресом в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="83ce5-127">Клиентская программа переходит в список до тех пор, пока не будет выполнено успешное подключение или не достигнет конца списка.</span><span class="sxs-lookup"><span data-stu-id="83ce5-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="83ce5-128">Обратите внимание, что если клиентская программа устанавливает успешное подключение, она не считывает ни одного из последующих URL-адресов в списке.</span><span class="sxs-lookup"><span data-stu-id="83ce5-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83ce5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="83ce5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83ce5-130">**Предыдущие версии метафайлов Windows Media (не рекомендуется)**</span><span class="sxs-lookup"><span data-stu-id="83ce5-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




