---
title: S (API-интерфейсы UPnP)
description: Содержит термины, связанные с UPnP, которые начинаются с буквы S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070970"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="61f84-103">S (API-интерфейсы UPnP)</span><span class="sxs-lookup"><span data-stu-id="61f84-103">S (UPnP APIs)</span></span>

<span data-ttu-id="61f84-104">Содержит термины, связанные с UPnP, которые начинаются с буквы S.</span><span class="sxs-lookup"><span data-stu-id="61f84-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="61f84-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [р](h-gly.md) . J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="61f84-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="61f84-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**служеб**</span><span class="sxs-lookup"><span data-stu-id="61f84-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="61f84-107">Служба — это логическая функциональная единица.</span><span class="sxs-lookup"><span data-stu-id="61f84-107">A service is a logical functional unit.</span></span> <span data-ttu-id="61f84-108">Службы предоставляют действия и моделируют некоторые или все состояния физического устройства с помощью переменных состояния.</span><span class="sxs-lookup"><span data-stu-id="61f84-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="61f84-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Описание службы**</span><span class="sxs-lookup"><span data-stu-id="61f84-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="61f84-110">Описание службы — это список действий, предоставляемых службой, и переменные состояния, связанные с действиями.</span><span class="sxs-lookup"><span data-stu-id="61f84-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="61f84-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**Объект службы**</span><span class="sxs-lookup"><span data-stu-id="61f84-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="61f84-112">Объект службы является представлением API контрольной точки для службы.</span><span class="sxs-lookup"><span data-stu-id="61f84-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="61f84-113">Объект службы реализует интерфейс [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="61f84-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="61f84-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**Тип службы**</span><span class="sxs-lookup"><span data-stu-id="61f84-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="61f84-115">Тип службы — это URN, идентифицирующий службу.</span><span class="sxs-lookup"><span data-stu-id="61f84-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="61f84-116">Между шаблоном службы UPnP и типом службы существует связь «один к одному».</span><span class="sxs-lookup"><span data-stu-id="61f84-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="61f84-117">Несколько стандартных типов служб определяются на форуме UPnP.</span><span class="sxs-lookup"><span data-stu-id="61f84-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="61f84-118">Типы служб представлены в формате urn: schemas-UPnP-org: Service: serviceType: версия.</span><span class="sxs-lookup"><span data-stu-id="61f84-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="61f84-119">Например, тип службы сканера может быть urn: schemas-UPnP-org: служба: сканер: 1.</span><span class="sxs-lookup"><span data-stu-id="61f84-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="61f84-120">Поставщики UPnP могут указывать дополнительные службы.</span><span class="sxs-lookup"><span data-stu-id="61f84-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="61f84-121">Такие службы обозначаются urn: domain-name: Service: serviceType: версия, где domain-name — это доменное имя, зарегистрированное для поставщика.</span><span class="sxs-lookup"><span data-stu-id="61f84-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="61f84-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**переменная состояния**</span><span class="sxs-lookup"><span data-stu-id="61f84-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="61f84-123">Переменная состояния — это часть данных, которая описывает некоторую часть состояния службы.</span><span class="sxs-lookup"><span data-stu-id="61f84-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




