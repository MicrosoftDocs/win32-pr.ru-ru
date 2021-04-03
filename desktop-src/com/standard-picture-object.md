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
# <a name="standard-picture-object"></a>Стандартный объект Picture

Стандартный объект изображения обеспечивает абстракцию, не зависящую от языка, для изображений GDI: точечные рисунки, значки, метафайлы и расширенные метафайлы. Как и в случае со стандартным объектом Font, система предоставляет стандартную реализацию этого объекта. Его основными интерфейсами являются [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) и [**ипиктуредисп**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), второй является производным от **IDispatch** для предоставления доступа к свойствам изображения через OLE-автоматизацию. Объект изображения создается с помощью [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

Объект Picture также поддерживает исходящий интерфейс [**ипропертинотифисинк**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , чтобы клиент мог определить, когда изменяются свойства изображения. Соответственно, объект Picture также поддерживает [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) и одну точку подключения для **ипропертинотифисинк**.

Объект Picture также поддерживает [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , так что он может сохранять и загружать данные из экземпляра [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Объект, который использует объект изображения, обычно сохраняет и загружает изображение как часть собственной обработки сохраняемости объекта. Функция [**олелоадпиктуре**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) упрощает создание объекта изображения на основе содержимого потока.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления](control-properties.md)
</dt> </dl>

 

 