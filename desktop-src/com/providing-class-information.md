---
title: Предоставление сведений о классе
description: Предоставление сведений о классе
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132931"
---
# <a name="providing-class-information"></a><span data-ttu-id="a9f39-103">Предоставление сведений о классе</span><span class="sxs-lookup"><span data-stu-id="a9f39-103">Providing Class Information</span></span>

<span data-ttu-id="a9f39-104">Часто бывает полезно, чтобы клиент объекта просматривает сведения о типе объекта.</span><span class="sxs-lookup"><span data-stu-id="a9f39-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="a9f39-105">При наличии идентификатора CLSID объекта клиент может найти библиотеку типов объекта с помощью записей реестра, а затем может проверить библиотеку типов для записи coclass в библиотеке, соответствующей идентификатору CLSID.</span><span class="sxs-lookup"><span data-stu-id="a9f39-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="a9f39-106">Однако не все объекты имеют CLSID, хотя им по-прежнему требуется предоставить информацию о типе.</span><span class="sxs-lookup"><span data-stu-id="a9f39-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="a9f39-107">Кроме того, удобно, чтобы клиент имел способ просто запросить объект для получения сведений о его типе, вместо того чтобы использовать все долгой для извлечения той же информации из записей реестра.</span><span class="sxs-lookup"><span data-stu-id="a9f39-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="a9f39-108">Эта возможность важна при работе с исходящими интерфейсами на подключаемых объектах.</span><span class="sxs-lookup"><span data-stu-id="a9f39-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="a9f39-109">(Дополнительные сведения о том, как подключаемые объекты обеспечивают такую возможность, см. в разделе [Использование IProvideClassInfo](using-iprovideclassinfo.md) .)</span><span class="sxs-lookup"><span data-stu-id="a9f39-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="a9f39-110">В таких случаях клиент может запросить объект для [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="a9f39-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="a9f39-111">Если эти интерфейсы существуют, клиент вызывает метод [**жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) для получения сведений о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a9f39-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="a9f39-112">При реализации интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) или [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)объект указывает, что он может предоставлять сведения о типе для всего класса; Это значит, что оно будет описывать в разделе его класса Library, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="a9f39-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="a9f39-113">[**Жетклассинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) возвращает указатель **ITypeInfo** , соответствующий сведениям о соклассах объекта.</span><span class="sxs-lookup"><span data-stu-id="a9f39-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="a9f39-114">С помощью этого указателя **ITypeInfo** клиент может изучить все входящие и исходящие определения интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="a9f39-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="a9f39-115">Объект также может предоставлять [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="a9f39-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="a9f39-116">Интерфейс **IProvideClassInfo2** — это простое расширение для интерфейса [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) , которое позволяет быстро и легко извлекать исходящие идентификаторы интерфейса объекта для набора событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9f39-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="a9f39-117">**IProvideClassInfo2** является производным от **IProvideClassInfo**.</span><span class="sxs-lookup"><span data-stu-id="a9f39-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9f39-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a9f39-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f39-119">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="a9f39-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




