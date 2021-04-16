---
description: Поиск секций во время активации
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Поиск секций во время активации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104557394"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="f418d-103">Поиск секций во время активации</span><span class="sxs-lookup"><span data-stu-id="f418d-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="f418d-104">Поиск нужной секции, в которой активируется компонент, зависит от следующих факторов.</span><span class="sxs-lookup"><span data-stu-id="f418d-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="f418d-105">Вызов функции и параметры, используемые в вызывающей программе для активации компонента</span><span class="sxs-lookup"><span data-stu-id="f418d-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="f418d-106">Является ли активируемый компонент локальным или удаленным</span><span class="sxs-lookup"><span data-stu-id="f418d-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="f418d-107">Внутреннее использование кэша секций</span><span class="sxs-lookup"><span data-stu-id="f418d-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="f418d-108">Вызывающая программа</span><span class="sxs-lookup"><span data-stu-id="f418d-108">The Calling Program</span></span>

<span data-ttu-id="f418d-109">COM+ выбирает секцию для активации компонента в зависимости от того, как вызывающая программа активирует компонент.</span><span class="sxs-lookup"><span data-stu-id="f418d-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="f418d-110">При выборе секции для активации компонентов можно выполнить три разных действия.</span><span class="sxs-lookup"><span data-stu-id="f418d-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="f418d-111">Выполняемое действие зависит от того, как вызывающая программа создает экземпляр объекта, т. е. является ли вызов функции моникером секции, который состоит из идентификатора секции и идентификатора CLSID или включает только идентификатор CLSID.</span><span class="sxs-lookup"><span data-stu-id="f418d-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="f418d-112">В следующей таблице показаны различные действия, которые может выполнять COM+ в порядке приоритета для определения местоположения секции.</span><span class="sxs-lookup"><span data-stu-id="f418d-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="f418d-113">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="f418d-113">Function call</span></span>                                                  | <span data-ttu-id="f418d-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="f418d-114">Parameter</span></span>                                                      | <span data-ttu-id="f418d-115">Действие COM+</span><span class="sxs-lookup"><span data-stu-id="f418d-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f418d-116">[**Кожетобжект**](/windows/desktop/api/objbase/nf-objbase-cogetobject) или **GetObject**</span><span class="sxs-lookup"><span data-stu-id="f418d-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="f418d-117">Моникер секции (включает идентификатор секции и CLSID)</span><span class="sxs-lookup"><span data-stu-id="f418d-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="f418d-118">Использует идентификатор секции, указанный в моникере секции.</span><span class="sxs-lookup"><span data-stu-id="f418d-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f418d-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="f418d-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="f418d-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="f418d-120">CLSID</span></span><br/>                                               | <span data-ttu-id="f418d-121">Использует идентификатор секции по умолчанию для раздела удостоверения пользователя или идентификатор секции, добавленный в контекст во время активации предыдущей версии компонента в том же процессе.</span><span class="sxs-lookup"><span data-stu-id="f418d-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="f418d-122">Действия COM+, перечисленные в предыдущей таблице, описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="f418d-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="f418d-123">Использование моникеров секций</span><span class="sxs-lookup"><span data-stu-id="f418d-123">Use of Partition Monikers</span></span>

<span data-ttu-id="f418d-124">Секцию можно явно выбрать в вызове функции с помощью *моникера секции*.</span><span class="sxs-lookup"><span data-stu-id="f418d-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="f418d-125">Моникер секции используется в коде для явного указания секции активированного компонента.</span><span class="sxs-lookup"><span data-stu-id="f418d-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="f418d-126">Если моникер секции используется для нахождение секции, активация происходит из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="f418d-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="f418d-127">То есть идентификатор секции, включенный в моникер, имеет приоритет над разделом пользователя по умолчанию или с ИДЕНТИФИКАТОРом секции, который существует в контексте вызывающего.</span><span class="sxs-lookup"><span data-stu-id="f418d-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="f418d-128">В коде C++ синтаксис для использования моникера секции выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f418d-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="f418d-129">В следующем примере показан фрагмент кода C++, в котором моникер секции используется в качестве аргумента функции [**кожетобжект**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :</span><span class="sxs-lookup"><span data-stu-id="f418d-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="f418d-130">В Visual Basic коде синтаксис для моникера секции выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f418d-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="f418d-131">В следующем примере показан фрагмент кода Visual Basic, в котором моникер секции используется в качестве аргумента функции **GetObject** :</span><span class="sxs-lookup"><span data-stu-id="f418d-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="f418d-132">Использование сопоставления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f418d-132">Use of Default Mapping</span></span>

<span data-ttu-id="f418d-133">Если функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) используется для активации компонента с помощью CLSID компонента, com+ использует сопоставление удостоверений пользователя по умолчанию, то есть набор секций, с которым пользователь сопоставлен в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f418d-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="f418d-134">Однако если пользователь не сопоставлен с набором разделов в Active Directory, выбирается глобальный раздел.</span><span class="sxs-lookup"><span data-stu-id="f418d-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="f418d-135">Использование идентификаторов секций и контекста объектов</span><span class="sxs-lookup"><span data-stu-id="f418d-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="f418d-136">Одним из пяти свойств, назначенных новой секции, является идентификатор секции.</span><span class="sxs-lookup"><span data-stu-id="f418d-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="f418d-137">Когда клиентская программа вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра объекта, идентификатор секции добавляется в контекст.</span><span class="sxs-lookup"><span data-stu-id="f418d-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="f418d-138">Использование идентификатора секции из контекста для нахождения секции имеет важное значение, так как гарантирует, что после начала цепочки активаций идентификатор секции остается прежним, если он не был явно изменен через моникер раздела.</span><span class="sxs-lookup"><span data-stu-id="f418d-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="f418d-139">Дополнительные сведения о расположении секций во время активации см. в разделе [com+ Queued Components and partitions](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="f418d-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="f418d-140">Локальная и удаленная активация</span><span class="sxs-lookup"><span data-stu-id="f418d-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="f418d-141">Если вызываемый компонент существует на другом компьютере, то свойства раздела (включая идентификатор секции) маршалируются на другой компьютер, а компонент активируется из упакованной секции.</span><span class="sxs-lookup"><span data-stu-id="f418d-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="f418d-142">Если идентификатор секции не был маршалирован, COM+ использует набор разделов по умолчанию, сопоставленный с удостоверением пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f418d-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="f418d-143">Кэш секций</span><span class="sxs-lookup"><span data-stu-id="f418d-143">The Partition Cache</span></span>

<span data-ttu-id="f418d-144">В среде домена COM+ использует сопоставления в Active Directory, чтобы выбрать правильный раздел для активации компонента.</span><span class="sxs-lookup"><span data-stu-id="f418d-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="f418d-145">Однако частое Поиск в Active Directory может привести к чрезмерному использованию сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="f418d-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="f418d-146">Для снижения сетевого трафика, полученного в результате частого поиска сопоставления "пользователь-Секция-набор" в Active Directory, COM+ использует *кэш секций*.</span><span class="sxs-lookup"><span data-stu-id="f418d-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="f418d-147">Кэш разделов содержит сопоставления, которые были сделаны в Active Directory между удостоверениями пользователей или подразделениями и их наборами секций.</span><span class="sxs-lookup"><span data-stu-id="f418d-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="f418d-148">Этот кэш разделов находится на сервере приложений, на котором находятся приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="f418d-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="f418d-149">Когда COM+ необходимо определить раздел пользователя по умолчанию или проверить права доступа пользователя к секции, он проверяет локальный кэш разделов для поиска сопоставления пользователя, а не проверяет Active Directory удаленно.</span><span class="sxs-lookup"><span data-stu-id="f418d-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="f418d-150">Если поиск в кэше секций завершается сбоем, COM+ проверяет Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f418d-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="f418d-151">Если поиск выполнен в Active Directory, COM+ сохраняет это сопоставление в кэше разделов.</span><span class="sxs-lookup"><span data-stu-id="f418d-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="f418d-152">При следующем выполнении уточняющего запроса для сопоставления пользователя и секции COM+ обнаружит его в кэше разделов.</span><span class="sxs-lookup"><span data-stu-id="f418d-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="f418d-153">На следующем рисунке показан процесс, используемый COM+ для размещения секции для активации компонента.</span><span class="sxs-lookup"><span data-stu-id="f418d-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Схема, на которой показано дерево устранения неполадок для процесса, используемого COM+ для поиска секции для активации компонента.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="f418d-155">Размер кэша и срок действия для записей кэша задаются с помощью разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="f418d-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="f418d-156">Сведения о настройке этих разделов реестра см. в разделе [Создание и Настройка разделов COM+](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="f418d-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="f418d-157">Если компьютер сервера отключается от сети и сопоставление пользователя с Секцией изменяется в то время, когда сервер отключен, то кэш разделов может содержать устаревшее сопоставление пользователя с секцией.</span><span class="sxs-lookup"><span data-stu-id="f418d-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="f418d-158">Это может привести к ошибке активации, если сопоставление пользователя с Секцией является механизмом, используемым для активации компонента.</span><span class="sxs-lookup"><span data-stu-id="f418d-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f418d-159">См. также</span><span class="sxs-lookup"><span data-stu-id="f418d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f418d-160">Поиск компонента для активации</span><span class="sxs-lookup"><span data-stu-id="f418d-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

