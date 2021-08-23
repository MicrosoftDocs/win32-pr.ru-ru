---
title: Стандартный объект Picture
description: Стандартный объект Picture
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4b74daa4f62791c12927eba3fd0472ed2a956d4b84c03e3cc373c44e12ce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129766"
---
# <a name="standard-picture-object"></a>Стандартный объект Picture

Стандартный объект изображения обеспечивает абстракцию, не зависящую от языка, для изображений GDI: точечные рисунки, значки, метафайлы и расширенные метафайлы. Как и в случае со стандартным объектом Font, система предоставляет стандартную реализацию этого объекта. Его основными интерфейсами являются [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) и [**ипиктуредисп**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), второй является производным от **IDispatch** для предоставления доступа к свойствам изображения через OLE-автоматизацию. Объект изображения создается с помощью [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

Объект Picture также поддерживает исходящий интерфейс [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , чтобы клиент мог определить, когда изменяются свойства изображения. Соответственно, объект Picture также поддерживает [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) и одну точку подключения для **ипропертинотифисинк**.

Объект Picture также поддерживает [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , так что он может сохранять и загружать данные из экземпляра [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Объект, который использует объект изображения, обычно сохраняет и загружает изображение как часть собственной обработки сохраняемости объекта. Функция [**олелоадпиктуре**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) упрощает создание объекта изображения на основе содержимого потока.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления](control-properties.md)
</dt> </dl>

 

 