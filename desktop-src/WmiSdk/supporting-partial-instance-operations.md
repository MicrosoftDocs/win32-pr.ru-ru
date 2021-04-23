---
description: Поставщик не требуется для поддержки каких-либо операций с частичным экземпляром. Однако поставщик должен либо поддерживать всю семантику операции частичного экземпляра, обрабатывать завершенный экземпляр, либо возвращать \_ \_ неподдерживаемый параметр WBEM E \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Поддержка операций Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701984"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="e2a06-104">Поддержка операций Partial-Instance</span><span class="sxs-lookup"><span data-stu-id="e2a06-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="e2a06-105">Поставщик не требуется для поддержки каких-либо операций с частичным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e2a06-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="e2a06-106">Однако поставщик должен либо поддерживать всю семантику операции частичного экземпляра, обрабатывать завершенный экземпляр, либо возвращать **\_ \_ неподдерживаемый \_ параметр WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="e2a06-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="e2a06-107">При создании поставщика, поддерживающего операции с частичным экземпляром, необходимо соблюдать следующие правила.</span><span class="sxs-lookup"><span data-stu-id="e2a06-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="e2a06-108">Повторно используйте тот же объект контекста, который WMI отправляет поставщику.</span><span class="sxs-lookup"><span data-stu-id="e2a06-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="e2a06-109">Инструментарий WMI использует \_ \_ \_ \_ именованное значение "получить ext Client \_ request" для предотвращения взаимоблокировок и удаления этого клиента перед пересылкой объекта контекста поставщику.</span><span class="sxs-lookup"><span data-stu-id="e2a06-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="e2a06-110">Для повторных вызовов в WMI, которые не нуждаются в операциях с частичным экземпляром, необходимо передать обратно тот же объект контекста без каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="e2a06-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="e2a06-111">Инструментарий WMI получает объект контекста без \_ \_ \_ \_ \_ набора именованных значений "получить ext Client Request" и удаляет все именованные значения, связанные с операциями частичного экземпляра, из объекта контекста перед передачей его другим поставщикам.</span><span class="sxs-lookup"><span data-stu-id="e2a06-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="e2a06-112">Если не изменить объект контекста, другие поставщики не получают операции получения частичного экземпляра, предназначенные для другого, несвязанного объекта.</span><span class="sxs-lookup"><span data-stu-id="e2a06-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="e2a06-113">Чтобы выполнить повторное выполнение операции частичного экземпляра во время выполнения запроса, установите отсутствующий параметр " \_ \_ получить \_ ext \_ Client \_ request" с именем и свойством Clear.</span><span class="sxs-lookup"><span data-stu-id="e2a06-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="e2a06-114">При необходимости можно изменить свойства в \_ \_ \_ \_ именованном значении "получить свойства ext" перед отправкой объекта контекста обратно в WMI с помощью повторного вызова.</span><span class="sxs-lookup"><span data-stu-id="e2a06-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="e2a06-115">Не обращаются к объекту контекста после возврата в WMI во время повторного вызова. другие поставщики могут изменять списки свойств или другие значения во время повторного входа.</span><span class="sxs-lookup"><span data-stu-id="e2a06-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="e2a06-116">Вы можете проверить или изменить объект контекста только на время реализации вызова [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="e2a06-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



