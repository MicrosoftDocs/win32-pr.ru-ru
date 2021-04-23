---
title: Создание и обслуживание точки подключения службы
description: При публикации с помощью точки подключения службы следует помнить, что она должна содержать текущие данные об экземпляре службы.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Создание и обслуживание точки подключения службы AD
- точка подключения службы AD, создание и обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069793"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="93739-105">Создание и обслуживание точки подключения службы</span><span class="sxs-lookup"><span data-stu-id="93739-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="93739-106">При публикации с помощью точки подключения службы следует помнить, что она должна содержать текущие данные об экземпляре службы.</span><span class="sxs-lookup"><span data-stu-id="93739-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="93739-107">В противном случае клиенты, которые привязываются к SCP, получают устаревшие данные.</span><span class="sxs-lookup"><span data-stu-id="93739-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="93739-108">Установщик службы, который создает SCP, задает начальные значения для атрибутов запрашивая.</span><span class="sxs-lookup"><span data-stu-id="93739-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="93739-109">Затем при запуске экземпляра службы он должен наыскать точку подключения службы и при необходимости обновить значения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="93739-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="93739-110">Таким образом, клиенты гарантированно используют самые актуальные данные.</span><span class="sxs-lookup"><span data-stu-id="93739-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="93739-111">После создания точки подключения службы установщик служб выполняет два дополнительных действия, которые позволяют службе обновить SCP.</span><span class="sxs-lookup"><span data-stu-id="93739-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="93739-112">Установите ACE в дескрипторе безопасности объекта SCP, чтобы служба изменила атрибуты SCP во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="93739-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="93739-113">Дополнительные сведения и пример кода см. в разделе [Включение учетной записи службы для доступа к свойствам SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="93739-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="93739-114">Кэширование **OBJECTGUID** SCP в реестре на главном компьютере службы.</span><span class="sxs-lookup"><span data-stu-id="93739-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="93739-115">Служба получает кэшированный идентификатор GUID для привязки к точке подключения службы, чтобы проверить и обновить ее атрибуты.</span><span class="sxs-lookup"><span data-stu-id="93739-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="93739-116">Установщик службы кэширует **OBJECTGUID** SCP, а не DN.</span><span class="sxs-lookup"><span data-stu-id="93739-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="93739-117">**ObjectGUID** никогда не изменяется, независимо от того, перемещена или переименована точка подключения службы.</span><span class="sxs-lookup"><span data-stu-id="93739-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="93739-118">DN может измениться, если администратор переместит или переименовывает точку подключения службы.</span><span class="sxs-lookup"><span data-stu-id="93739-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="93739-119">Например, если точка подключения службы создается как дочерний объект компьютера, различающееся имя SCP изменится, если компьютер переименовывается или перемещается в другой домен или подразделение.</span><span class="sxs-lookup"><span data-stu-id="93739-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="93739-120">Когда установщик службы создает SCP, он должен прочитать **objectGUID** созданного объекта и кэшировать его в реестре главного компьютера службы.</span><span class="sxs-lookup"><span data-stu-id="93739-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="93739-121">Используйте метод [**iAds:: Get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) , чтобы получить значение **objectGUID** в строковом формате, подходящем для привязки.</span><span class="sxs-lookup"><span data-stu-id="93739-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="93739-122">Кэшировать строку GUID как значение в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="93739-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="93739-123">Где "имя поставщика" и "название продукта" обозначают поставщика и продукт.</span><span class="sxs-lookup"><span data-stu-id="93739-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="93739-124">При запуске служба получает кэшированную строку GUID из реестра и использует ее для привязки к точке подключения службы.</span><span class="sxs-lookup"><span data-stu-id="93739-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="93739-125">Служба считывает важные атрибуты SCP и сравнивает их с текущими значениями.</span><span class="sxs-lookup"><span data-stu-id="93739-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="93739-126">Если значения SCP устарели, служба обновляет их.</span><span class="sxs-lookup"><span data-stu-id="93739-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="93739-127">Значения, которые может потребоваться службе для обновления, включают **Ключевые слова**, **сервицебиндингинформатион**, **serviceDNSName** и **сервицеднснаметипе**.</span><span class="sxs-lookup"><span data-stu-id="93739-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="93739-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="93739-128">Examples</span></span>

-   [<span data-ttu-id="93739-129">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="93739-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="93739-130">Примеры кода (C/C++)</span><span class="sxs-lookup"><span data-stu-id="93739-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 