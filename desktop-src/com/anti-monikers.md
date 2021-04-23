---
title: Специальные имена
description: OLE предоставляет реализацию специального типа моникера, который называется Anti-моникером.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068113"
---
# <a name="anti-monikers"></a><span data-ttu-id="dead6-103">Специальные имена</span><span class="sxs-lookup"><span data-stu-id="dead6-103">Anti-Monikers</span></span>

<span data-ttu-id="dead6-104">OLE предоставляет реализацию специального типа моникера, который называется *Anti-моникером*.</span><span class="sxs-lookup"><span data-stu-id="dead6-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="dead6-105">Это специальное имя используется при создании новых классов моникера.</span><span class="sxs-lookup"><span data-stu-id="dead6-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="dead6-106">Он используется в качестве обратного моникера, в котором оно состоит, что фактически отменяет этот моникер во многом так же, как оператор ".." перемещает уровень каталога вверх в команде файловой системы.</span><span class="sxs-lookup"><span data-stu-id="dead6-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="dead6-107">Необходимо иметь доступ к борьбе с моникером, поскольку после создания составного моникера невозможно удалить части моникера, если, например, объект будет перемещен.</span><span class="sxs-lookup"><span data-stu-id="dead6-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="dead6-108">Вместо этого для удаления одной или нескольких записей из составного моникера используется защита моникера.</span><span class="sxs-lookup"><span data-stu-id="dead6-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="dead6-109">Защита моникеров — это класс моникера, явно предназначенный для использования в качестве обратного.</span><span class="sxs-lookup"><span data-stu-id="dead6-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="dead6-110">COM определяет именованную функцию [**креатеантимоникер**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) , которая возвращает средство защиты моникера.</span><span class="sxs-lookup"><span data-stu-id="dead6-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="dead6-111">Обычно эта функция используется для реализации метода [**IMoniker:: инверсии**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .</span><span class="sxs-lookup"><span data-stu-id="dead6-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="dead6-112">Для тех типов моникеров, которые реализуются как обратные, применяются только обратные моникеры.</span><span class="sxs-lookup"><span data-stu-id="dead6-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="dead6-113">Например, если вы хотите удалить последнюю часть составного моникера, не создавайте и составьте моникер в конце составного.</span><span class="sxs-lookup"><span data-stu-id="dead6-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="dead6-114">Нельзя гарантировать, что в последнем фрагменте составного моникера рассматривается как обратное.</span><span class="sxs-lookup"><span data-stu-id="dead6-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="dead6-115">Вместо этого следует вызвать [**IMoniker:: Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) для составного моникера, указав в качестве первого параметра **значение false** .</span><span class="sxs-lookup"><span data-stu-id="dead6-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="dead6-116">При этом создается перечислитель, который возвращает моникеры компонента в обратный порядок.</span><span class="sxs-lookup"><span data-stu-id="dead6-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="dead6-117">Используйте перечислитель для получения последней части составного элемента и выполните [**обратный**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) вызов для этого моникера.</span><span class="sxs-lookup"><span data-stu-id="dead6-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="dead6-118">Моникер, возвращаемый **инверсией** , — это то, что необходимо для удаления последнего фрагмента составного.</span><span class="sxs-lookup"><span data-stu-id="dead6-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dead6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dead6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dead6-120">Моникеры класса</span><span class="sxs-lookup"><span data-stu-id="dead6-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="dead6-121">Составные моникеры</span><span class="sxs-lookup"><span data-stu-id="dead6-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="dead6-122">Моникеры файлов</span><span class="sxs-lookup"><span data-stu-id="dead6-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="dead6-123">Моникеры элементов</span><span class="sxs-lookup"><span data-stu-id="dead6-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="dead6-124">Моникеры указателей</span><span class="sxs-lookup"><span data-stu-id="dead6-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




