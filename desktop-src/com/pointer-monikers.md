---
title: Моникеры указателей
description: Моникер указателя определяет объект, который может существовать только в активном или выполняющемся состоянии. Это отличается от других классов моникеров, которые указывают объекты, которые могут существовать либо в пассивном, либо в активном состоянии.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "104412386"
---
# <a name="pointer-monikers"></a><span data-ttu-id="15674-104">Моникеры указателей</span><span class="sxs-lookup"><span data-stu-id="15674-104">Pointer Monikers</span></span>

<span data-ttu-id="15674-105">*Моникер указателя* определяет объект, который может существовать только в активном или выполняющемся состоянии.</span><span class="sxs-lookup"><span data-stu-id="15674-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="15674-106">Это отличается от других классов моникеров, которые указывают объекты, которые могут существовать либо в пассивном, либо в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="15674-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="15674-107">Предположим, например, что приложение имеет объект, который не имеет постоянного представления.</span><span class="sxs-lookup"><span data-stu-id="15674-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="15674-108">Как правило, если клиенту приложения требуется доступ к этому объекту, можно просто передать клиенту указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="15674-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="15674-109">Однако предположим, что клиент ожидает моникер.</span><span class="sxs-lookup"><span data-stu-id="15674-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="15674-110">Объект не может быть идентифицирован с помощью моникера файла, так как он не хранится в файле или с моникером элемента, поскольку он не содержится в другом объекте.</span><span class="sxs-lookup"><span data-stu-id="15674-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="15674-111">Вместо этого приложение может создать моникер указателя, который является моникером, который просто содержит указатель мыши, и передать его клиенту.</span><span class="sxs-lookup"><span data-stu-id="15674-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="15674-112">Клиент может рассматривать это специальное имя как угодно.</span><span class="sxs-lookup"><span data-stu-id="15674-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="15674-113">Однако когда клиент вызывает [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) в моникере указателя, код моникера не проверяет работу таблицы ROT или не загружает что-либо из хранилища.</span><span class="sxs-lookup"><span data-stu-id="15674-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="15674-114">Вместо этого код моникера просто вызывает [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для указателя, хранящегося внутри моникера.</span><span class="sxs-lookup"><span data-stu-id="15674-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="15674-115">Моникеры указателей позволяют объектам, которые существуют только в активном или выполняющемся состоянии, участвовать в операциях моникера и использоваться клиентами моникера.</span><span class="sxs-lookup"><span data-stu-id="15674-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="15674-116">Одно важное различие между моникерами указателя и другими классами моникеров заключается в том, что моникеры указателей не могут быть сохранены в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="15674-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="15674-117">В этом случае вызов метода [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="15674-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="15674-118">Это означает, что моникеры указателей полезны только в специализированных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="15674-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="15674-119">Если необходимо использовать моникер указателя, можно использовать функцию [**креатепоинтермоникер**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) .</span><span class="sxs-lookup"><span data-stu-id="15674-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15674-120">См. также</span><span class="sxs-lookup"><span data-stu-id="15674-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15674-121">Специальные имена</span><span class="sxs-lookup"><span data-stu-id="15674-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="15674-122">Моникеры класса</span><span class="sxs-lookup"><span data-stu-id="15674-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="15674-123">Составные моникеры</span><span class="sxs-lookup"><span data-stu-id="15674-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="15674-124">Моникеры файлов</span><span class="sxs-lookup"><span data-stu-id="15674-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="15674-125">Моникеры элементов</span><span class="sxs-lookup"><span data-stu-id="15674-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




