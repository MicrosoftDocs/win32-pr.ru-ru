---
description: Компонент, имеющий по крайней мере один интерфейс куеуабле, является компонентом куеуабле.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Создание компонентов Куеуабле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423341"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="0acbc-103">Создание компонентов Куеуабле</span><span class="sxs-lookup"><span data-stu-id="0acbc-103">Creating Queuable Components</span></span>

<span data-ttu-id="0acbc-104">Компонент, имеющий по крайней мере один интерфейс куеуабле, является *компонентом куеуабле*.</span><span class="sxs-lookup"><span data-stu-id="0acbc-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="0acbc-105">Чтобы компонент вызывался очередью, интерфейсы должны быть помечены как куеуабле, а компонент должен быть установлен в очереди приложения.</span><span class="sxs-lookup"><span data-stu-id="0acbc-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="0acbc-106">Однако компонент куеуабле может быть компонентом приложения без очереди.</span><span class="sxs-lookup"><span data-stu-id="0acbc-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="0acbc-107">Интерфейс куеуабле должен содержать только параметры in — без параметров out и без возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="0acbc-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="0acbc-108">Эти характеристики проверяются путем анализа сведений о типе во время установки компонента.</span><span class="sxs-lookup"><span data-stu-id="0acbc-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="0acbc-109">Если интерфейс не куеуабле, то очередь приложения, содержащей компонент, не может быть активирована.</span><span class="sxs-lookup"><span data-stu-id="0acbc-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="0acbc-110">Чтобы указать интерфейс COM+ в качестве куеуабле, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0acbc-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="0acbc-111">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым вы хотите управлять.</span><span class="sxs-lookup"><span data-stu-id="0acbc-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="0acbc-112">Откройте папку **интерфейсы** компонента приложения COM+, которое требуется сделать куеуабле.</span><span class="sxs-lookup"><span data-stu-id="0acbc-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="0acbc-113">Щелкните правой кнопкой мыши интерфейс, который нужно пометить как куеуабле, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="0acbc-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="0acbc-114">Выберите вкладку **очередь** в диалоговом окне Свойства.</span><span class="sxs-lookup"><span data-stu-id="0acbc-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="0acbc-115">Активируйте флажок с меткой **поставлено в очередь**.</span><span class="sxs-lookup"><span data-stu-id="0acbc-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="0acbc-116">Если флажок в **очереди** неактивен, интерфейс не удовлетворяет описанным выше ограничениям куеуабле.</span><span class="sxs-lookup"><span data-stu-id="0acbc-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="0acbc-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0acbc-117">Click **OK**.</span></span>

    <span data-ttu-id="0acbc-118">Компонент куеуабле может быть идентифицирован таким образом, добавляя макрос атрибута QUEUEd в раздел Interface исходного файла IDL для всех интерфейсов, куеуабле.</span><span class="sxs-lookup"><span data-stu-id="0acbc-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="0acbc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0acbc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0acbc-120">Создание очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="0acbc-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="0acbc-121">Разработка компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="0acbc-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



