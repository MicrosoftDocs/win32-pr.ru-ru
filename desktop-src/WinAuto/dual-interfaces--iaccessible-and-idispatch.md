---
title: Сдвоенные интерфейсы IAccessible и IDispatch
description: Разработчикам сервера необходимо предоставить интерфейс IDispatch интерфейса (COM) уровня "Стандартный" для доступных объектов.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700873"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="f8978-103">Сдвоенные интерфейсы: IAccessible и IDispatch</span><span class="sxs-lookup"><span data-stu-id="f8978-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="f8978-104">Разработчикам сервера необходимо предоставить интерфейс [**IDispatch**](idispatch-interface.md) интерфейса (com) уровня "Стандартный" для доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="f8978-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="f8978-105">Интерфейс IDispatch позволяет клиентским приложениям, написанным на Microsoft Visual Basic и различным языкам сценариев, использовать методы и свойства, предоставляемые методом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="f8978-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="f8978-106">Так как доступный объект предоставляет доступ к объекту непрямо через [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) или напрямую с **IAccessible**, говорят, что у него есть сдвоенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f8978-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="f8978-107">Когда клиенты C/C++ получают указатель интерфейса IDispatch, клиенты могут вызвать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы попробовать преобразовать указатель интерфейса IDispatch в указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="f8978-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="f8978-108">Чтобы вызывать методы **IAccessible** косвенно, клиенты C/C++ вызывают IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="f8978-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="f8978-109">Для повышения производительности вызывайте методы **IAccessible** для непосредственного использования объекта.</span><span class="sxs-lookup"><span data-stu-id="f8978-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="f8978-110">Список идентификаторов диспетчеризации (DISPID), которые интерфейс **IDispatch** использует для идентификации методов и свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , см. [в приложении C: идентификаторы DISPID](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="f8978-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="f8978-111">В версии 2,0 и более поздних версиях Microsoft Active Accessibility серверы не обязательно полностью реализуют методы [**IDispatch**](idispatch-interface.md) , но могут просто возвращать E \_ нотимпл после инициализации параметров out, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="f8978-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 