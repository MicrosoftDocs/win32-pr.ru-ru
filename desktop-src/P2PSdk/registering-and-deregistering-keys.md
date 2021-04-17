---
description: Регистрация и Отмена регистрации ключей
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Регистрация и Отмена регистрации ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663966"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="65d12-103">Регистрация и Отмена регистрации ключей</span><span class="sxs-lookup"><span data-stu-id="65d12-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="65d12-104">Регистрация ключей</span><span class="sxs-lookup"><span data-stu-id="65d12-104">Registering Keys</span></span>

<span data-ttu-id="65d12-105">Узел может регистрировать ключи в [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey) в любое время в **\_ режиме DRT Active**, **DRT \_** и **DRT \_ без \_ сетевого** состояния.</span><span class="sxs-lookup"><span data-stu-id="65d12-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="65d12-106">Ключи, регистрируемые **\_ только в DRT** , и **DRT \_ не \_** могут быть распознаны другими ДРТС после перехода локального узла в **DRT \_ Active**.</span><span class="sxs-lookup"><span data-stu-id="65d12-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="65d12-107">Идентичные ключи не могут быть зарегистрированы в одном экземпляре DRT при использовании [**дрткреатедериведкэйсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span><span class="sxs-lookup"><span data-stu-id="65d12-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="65d12-108">При попыток регистрации идентичных ключей Регистрация второго ключа завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="65d12-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="65d12-109">Использование идентичных ключей также следует избегать между разными экземплярами DRT.</span><span class="sxs-lookup"><span data-stu-id="65d12-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="65d12-110">Поиск по уникальному ключу. Эти идентичные ключи могут возвращать любой из ключей, независимо от того, какие данные связаны с ключом.</span><span class="sxs-lookup"><span data-stu-id="65d12-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="65d12-111">Если для реализации требуется другое поведение, можно создать поставщик безопасности вместо [**дрткреатедериведкэйсекуритипровидер**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) для размещения.</span><span class="sxs-lookup"><span data-stu-id="65d12-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="65d12-112">Отмена регистрации ключей</span><span class="sxs-lookup"><span data-stu-id="65d12-112">Deregistering Keys</span></span>

<span data-ttu-id="65d12-113">Узел может отменить регистрацию ключа в любое время после его регистрации.</span><span class="sxs-lookup"><span data-stu-id="65d12-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="65d12-114">Однако только приложение, которое зарегистрировало ключ, может отменить его регистрацию.</span><span class="sxs-lookup"><span data-stu-id="65d12-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="65d12-115">Приложение может отменить регистрацию ключа на локальном узле с помощью функции [**дртунрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) .</span><span class="sxs-lookup"><span data-stu-id="65d12-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="65d12-116">По завершении функция активирует событие **\_ \_ \_ \_ изменения ключа конечного элемента DRT Event** , уведомляя приложение, а также другие узлы, участвующие в сетке DRT.</span><span class="sxs-lookup"><span data-stu-id="65d12-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="65d12-117">В состоянии **\_ сбоя DRT** , требуемый вызов [**дртклосе**](/windows/desktop/api/drt/nf-drt-drtclose) , приведет к отмене регистрации всех ключей в инфраструктуре DRT.</span><span class="sxs-lookup"><span data-stu-id="65d12-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65d12-118">См. также</span><span class="sxs-lookup"><span data-stu-id="65d12-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d12-119">Поиск в таблице распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="65d12-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="65d12-120">Сведения о таблицах распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="65d12-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="65d12-121">Справочник по распределенной маршрутизации API таблиц</span><span class="sxs-lookup"><span data-stu-id="65d12-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



