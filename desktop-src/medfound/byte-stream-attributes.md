---
description: Атрибуты потока байтов
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Атрибуты потока байтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692087"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="595cf-103">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="595cf-103">Byte Stream Attributes</span></span>

<span data-ttu-id="595cf-104">Следующие атрибуты применяются к некоторым потокам байтов.</span><span class="sxs-lookup"><span data-stu-id="595cf-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="595cf-105">Чтобы узнать, поддерживает ли байтовый поток атрибуты, запросите объект потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="595cf-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="595cf-106">attribute</span><span class="sxs-lookup"><span data-stu-id="595cf-106">Attribute</span></span>                                                                                  | <span data-ttu-id="595cf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="595cf-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="595cf-108">**\_ \_ тип содержимого MF \_ BYTESTREAM**</span><span class="sxs-lookup"><span data-stu-id="595cf-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="595cf-109">Указывает тип MIME потока байтов.</span><span class="sxs-lookup"><span data-stu-id="595cf-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="595cf-110">**\_Длительность BYTESTREAM \_ MF**</span><span class="sxs-lookup"><span data-stu-id="595cf-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="595cf-111">Задает длительность потока байтов в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="595cf-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="595cf-112">\_ \_ \_ URI файла ИФО BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="595cf-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="595cf-113">Указывает URL-адрес связанного файла ИФО.</span><span class="sxs-lookup"><span data-stu-id="595cf-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="595cf-114">**MF \_ BYTESTREAM \_ \_ время последнего изменения \_**</span><span class="sxs-lookup"><span data-stu-id="595cf-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="595cf-115">Указывает, когда байтовый поток был изменен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="595cf-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="595cf-116">**\_ \_ имя источника MF \_ BYTESTREAM**</span><span class="sxs-lookup"><span data-stu-id="595cf-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="595cf-117">Задает исходный URL-адрес для потока байтов.</span><span class="sxs-lookup"><span data-stu-id="595cf-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="595cf-118">Следующие атрибуты применяются к обработчикам потока байтов.</span><span class="sxs-lookup"><span data-stu-id="595cf-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="595cf-119">attribute</span><span class="sxs-lookup"><span data-stu-id="595cf-119">Attribute</span></span>                                                                                    | <span data-ttu-id="595cf-120">Описание</span><span class="sxs-lookup"><span data-stu-id="595cf-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="595cf-121">MF \_ битестреамхандлер \_ принимает \_ общий доступ к \_ записи</span><span class="sxs-lookup"><span data-stu-id="595cf-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="595cf-122">Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком.</span><span class="sxs-lookup"><span data-stu-id="595cf-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="595cf-123">См. также</span><span class="sxs-lookup"><span data-stu-id="595cf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="595cf-124">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="595cf-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="595cf-125">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="595cf-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



