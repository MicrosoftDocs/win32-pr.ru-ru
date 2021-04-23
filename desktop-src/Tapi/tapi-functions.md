---
description: В следующих разделах содержится алфавитный список функций, сгруппированных по областям. Сведения для каждой функции включают список допустимых состояний вызова для записи функции и типичные переходы состояния вызова по завершении запроса.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Функции TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545642"
---
# <a name="tapi-functions"></a><span data-ttu-id="cbac2-104">Функции TAPI</span><span class="sxs-lookup"><span data-stu-id="cbac2-104">TAPI Functions</span></span>

<span data-ttu-id="cbac2-105">В следующих разделах содержится алфавитный список функций, сгруппированных по областям.</span><span class="sxs-lookup"><span data-stu-id="cbac2-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="cbac2-106">Сведения для каждой функции включают список допустимых состояний вызова для записи функции и типичные переходы состояния вызова по завершении запроса.</span><span class="sxs-lookup"><span data-stu-id="cbac2-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="cbac2-107">Функции телефонной связи</span><span class="sxs-lookup"><span data-stu-id="cbac2-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="cbac2-108">Функции центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="cbac2-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="cbac2-109">Функции линейного устройства</span><span class="sxs-lookup"><span data-stu-id="cbac2-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="cbac2-110">Функции телефонных устройств</span><span class="sxs-lookup"><span data-stu-id="cbac2-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="cbac2-111">Сведения о функциях TAPI, упорядоченных по уровням обслуживания и задачам, см. в разделе [Справочник по быстрой функции TAPI](tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cbac2-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="cbac2-112">Обратите внимание, что в отношении реальных состояний, в которых может быть выполнена функция, могут существовать ограничения поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="cbac2-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="cbac2-113">Приложения должны проверить элемент **двкаллфеатурес** в структуре [**Линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , элемент **дваддрессфеатурес** в структуре [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) и элемент **двлинефеатурес** в структуре [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , чтобы определить, разрешена ли функция в текущем состоянии вызова.</span><span class="sxs-lookup"><span data-stu-id="cbac2-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



