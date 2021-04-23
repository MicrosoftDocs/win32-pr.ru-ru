---
title: Стандартный объект Picture
description: Стандартный объект Picture
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987913"
---
# <a name="standard-picture-object"></a><span data-ttu-id="ad1c3-103">Стандартный объект Picture</span><span class="sxs-lookup"><span data-stu-id="ad1c3-103">Standard Picture Object</span></span>

<span data-ttu-id="ad1c3-104">Стандартный объект изображения обеспечивает абстракцию, не зависящую от языка, для изображений GDI: точечные рисунки, значки, метафайлы и расширенные метафайлы.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="ad1c3-105">Как и в случае со стандартным объектом Font, система предоставляет стандартную реализацию этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="ad1c3-106">Его основными интерфейсами являются [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) и [**ипиктуредисп**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), второй является производным от **IDispatch** для предоставления доступа к свойствам изображения через OLE-автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="ad1c3-107">Объект изображения создается с помощью [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="ad1c3-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="ad1c3-108">Объект Picture также поддерживает исходящий интерфейс [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , чтобы клиент мог определить, когда изменяются свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="ad1c3-109">Соответственно, объект Picture также поддерживает [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) и одну точку подключения для **ипропертинотифисинк**.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="ad1c3-110">Объект Picture также поддерживает [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , так что он может сохранять и загружать данные из экземпляра [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="ad1c3-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="ad1c3-111">Объект, который использует объект изображения, обычно сохраняет и загружает изображение как часть собственной обработки сохраняемости объекта.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="ad1c3-112">Функция [**олелоадпиктуре**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) упрощает создание объекта изображения на основе содержимого потока.</span><span class="sxs-lookup"><span data-stu-id="ad1c3-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad1c3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ad1c3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad1c3-114">Свойства элемента управления</span><span class="sxs-lookup"><span data-stu-id="ad1c3-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 