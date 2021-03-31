---
title: Параметр Мсвмекст (не рекомендуется)
description: Параметр Мсвмекст (не рекомендуется)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Метафайлы Windows Media, параметр Мсвмекст
- Метафайлы, параметр Мсвмекст
- Мсвмекст, параметр
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412603"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="2dece-106">Параметр Мсвмекст (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="2dece-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="2dece-107">Параметр *мсвмекст* указывает клиентскому приложению формат файла, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="2dece-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="2dece-108">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="2dece-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="2dece-109">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="2dece-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="2dece-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dece-110">Remarks</span></span>

<span data-ttu-id="2dece-111">Клиентские программы иногда используют расширение имени файла или тип MIME, чтобы определить, следует ли визуализировать файл мультимедиа в виде потока, подготовить файл после полной загрузки или отказаться от подготовки к просмотру файла.</span><span class="sxs-lookup"><span data-stu-id="2dece-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="2dece-112">Если клиентская программа не может определить, как обрабатывать файл мультимедиа на основе расширения имени файла или типа MIME, он может определить, как обрабатывать файл, проверив параметр *мсвмекст* .</span><span class="sxs-lookup"><span data-stu-id="2dece-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="2dece-113">Например, клиент может обрабатывать файл так, как если бы он имел расширение, равное значению параметра *мсвмекст* .</span><span class="sxs-lookup"><span data-stu-id="2dece-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="2dece-114">Дополнительные сведения о типах MIME и расширениях имен файлов см. в разделе [расширения имен файлов](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="2dece-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="2dece-115">Дополнительные сведения о параметре *мсвмекст* см. в статье [236895](https://support.microsoft.com/kb/236895) базы знаний Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2dece-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dece-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2dece-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dece-117">**Предыдущие версии метафайлов Windows Media (не рекомендуется)**</span><span class="sxs-lookup"><span data-stu-id="2dece-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




