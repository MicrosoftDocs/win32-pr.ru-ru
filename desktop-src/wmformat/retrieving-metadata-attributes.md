---
title: Получение атрибутов метаданных
description: Получение атрибутов метаданных
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Пакет SDK для формата Windows Media, извлечение атрибутов метаданных
- Расширенный системный формат (ASF), извлечение атрибутов метаданных
- ASF (Расширенный системный формат), извлечение атрибутов метаданных
- метаданные, извлечение атрибутов
- потоки, получение атрибутов метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069532"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="5e568-108">Получение атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="5e568-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="5e568-109">Чтобы получить атрибут из заголовка файла, необходимо узнать номер потока и индекс атрибута.</span><span class="sxs-lookup"><span data-stu-id="5e568-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="5e568-110">Чтобы получить индексы для всех атрибутов с одинаковым именем или всеми индексами на одном языке, можно использовать метод [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) .</span><span class="sxs-lookup"><span data-stu-id="5e568-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="5e568-111">Как и другие методы [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **жетаттрибутеиндицес** работает с одним потоком или со всеми атрибутами уровня файла, использующими поток 0.</span><span class="sxs-lookup"><span data-stu-id="5e568-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="5e568-112">Можно использовать значение 0xFFFF для номера потока, чтобы получить глобальные индексы, соответствующие критерию во всем файле, независимо от номера потока.</span><span class="sxs-lookup"><span data-stu-id="5e568-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="5e568-113">Если вы узнали индекс атрибута, который необходимо получить, вызовите метод [**IWMHeaderInfo3:: жетаттрибутебиндексекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) , чтобы получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="5e568-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="5e568-114">Для каждого полученного атрибута необходимо выполнить два вызова **жетаттрибутебиндексекс** .</span><span class="sxs-lookup"><span data-stu-id="5e568-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="5e568-115">При первом вызове передайте **значение NULL** для указателей имени и буфера данных, чтобы получить необходимый размер.</span><span class="sxs-lookup"><span data-stu-id="5e568-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="5e568-116">Затем выделите буферы указанного размера и выполните второй вызов, чтобы получить имя и данные.</span><span class="sxs-lookup"><span data-stu-id="5e568-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="5e568-117">Пример кода, показывающий, как получить атрибуты метаданных, см. [в разделе Извлечение всех метаданных в файле](to-retrieve-all-metadata-in-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="5e568-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e568-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5e568-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e568-119">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="5e568-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




