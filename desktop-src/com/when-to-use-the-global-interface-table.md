---
title: Когда следует использовать глобальную таблицу интерфейса
description: Когда следует использовать глобальную таблицу интерфейса
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070665"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="08074-103">Когда следует использовать глобальную таблицу интерфейса</span><span class="sxs-lookup"><span data-stu-id="08074-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="08074-104">Если вы размаршалирует указатель интерфейса несколько раз между апартаментами в процессе, то можете использовать интерфейс [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="08074-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="08074-105">При использовании других методов пришлось бы перемаршалировать каждый раз.</span><span class="sxs-lookup"><span data-stu-id="08074-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="08074-106">Если указатель интерфейса выполняется только один раз, может потребоваться использовать функцию [**комаршалинтерсреадинтерфацеинстреам**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) .</span><span class="sxs-lookup"><span data-stu-id="08074-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="08074-107">Он также может использоваться для передачи указателя интерфейса из одного потока в другой поток в том же процессе.</span><span class="sxs-lookup"><span data-stu-id="08074-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="08074-108">Интерфейс [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) также упрощает для программиста еще и более простую задачу.</span><span class="sxs-lookup"><span data-stu-id="08074-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="08074-109">Эта проблема возникает при выполнении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="08074-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="08074-110">Внутрипроцессный объект Agile выполняет статистическую обработку свободных потоков.</span><span class="sxs-lookup"><span data-stu-id="08074-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="08074-111">Этот же гибкий объект также содержит указатели интерфейсов (в виде переменных-членов) на другие объекты, которые не являются гибкими и не выполняют статистическую обработку для модуля упаковки с произвольным потоком.</span><span class="sxs-lookup"><span data-stu-id="08074-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="08074-112">В такой ситуации, если внешний объект маршалируется в другое подразделение и приложение вызывает его, и объект пытается вызвать для любого из его указателей интерфейса переменной-члена, которые не являются потокобезопасными или являются прокси для объектов в других подразделениях, может получить неверные результаты или ошибку RPC \_ E \_ неправильный \_ поток.</span><span class="sxs-lookup"><span data-stu-id="08074-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="08074-113">Эта ошибка возникает из-за того, что внутренний интерфейс предназначен для вызываемого только из апартамента, в котором он был первоначально сохранен в переменной-члене.</span><span class="sxs-lookup"><span data-stu-id="08074-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="08074-114">Чтобы решить эту проблему, внешний объект, который выполняет статистическую обработку свободных потоков, должен вызвать [**иглобалинтерфацетабле:: регистеринтерфацеинглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) во внутреннем интерфейсе и сохранить полученный файл cookie в его переменной-члене вместо того, чтобы хранить фактический указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="08074-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="08074-115">Когда внешний объект хочет вызвать указатель интерфейса внутреннего объекта, он должен вызвать [**иглобалинтерфацетабле:: жетинтерфацефромглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), использовать возвращаемый указатель интерфейса, а затем освободить его.</span><span class="sxs-lookup"><span data-stu-id="08074-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="08074-116">Когда внешний объект исчезает, он должен вызвать метод [**иглобалинтерфацетабле:: ревокеинтерфацефромглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) , чтобы удалить интерфейс из глобальной таблицы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="08074-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08074-117">См. также</span><span class="sxs-lookup"><span data-stu-id="08074-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08074-118">Создание глобальной таблицы интерфейса</span><span class="sxs-lookup"><span data-stu-id="08074-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 