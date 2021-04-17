---
description: Следующие термины полезны для понимания технологии TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684665"
---
# <a name="s-telephony-api"></a><span data-ttu-id="74402-103">S (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="74402-103">S (Telephony API)</span></span>

<span data-ttu-id="74402-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [р](h-tapgloss.md) [.](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="74402-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="74402-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**поставщик услуг**</span><span class="sxs-lookup"><span data-stu-id="74402-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="74402-106">Библиотека динамической компоновки, которая поддерживает связь по телефонной сети с помощью набора экспортированных функций службы.</span><span class="sxs-lookup"><span data-stu-id="74402-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="74402-107">Поставщик услуг отвечает на запросы телефонии, отправляемые ей через библиотеку динамической компоновки TAPI, выполнив низкоуровневые задачи, необходимые для взаимодействия по телефонной сети.</span><span class="sxs-lookup"><span data-stu-id="74402-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="74402-108">Таким образом, поставщик услуг в сочетании с TAPI изолирует приложения от сведений о связи телефонной сети, зависящих от службы и технологии.</span><span class="sxs-lookup"><span data-stu-id="74402-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="74402-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**подадресы**</span><span class="sxs-lookup"><span data-stu-id="74402-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="74402-110">Возможность, предоставляемая в линиях ISDN, которая позволяет использовать больше информации, чем единственный номер телефона, используемый при наборе номера.</span><span class="sxs-lookup"><span data-stu-id="74402-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="74402-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Дополнительная телефония**</span><span class="sxs-lookup"><span data-stu-id="74402-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="74402-112">Уровень обслуживания, предоставляющий расширенные функции коммутатора, такие как удержание, перенос и т. д.</span><span class="sxs-lookup"><span data-stu-id="74402-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="74402-113">Все дополнительные службы необязательны; то есть поставщик услуг не должен поддерживать их.</span><span class="sxs-lookup"><span data-stu-id="74402-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="74402-114">См. раздел [*Техническая*](a-tapgloss.md)Телефония, [*Базовая телефония*](b-tapgloss.md), [*Расширенная телефония*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span><span class="sxs-lookup"><span data-stu-id="74402-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="74402-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Переключенный 56**</span><span class="sxs-lookup"><span data-stu-id="74402-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="74402-116">Коммутируемая служба данных, которая позволяет пользователю звонить другим пользователям и передавать данные на полный дуплекс, цифровое синхронное 56 кбит/с за цену телефонного звонка.</span><span class="sxs-lookup"><span data-stu-id="74402-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="74402-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**рабатывают**</span><span class="sxs-lookup"><span data-stu-id="74402-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="74402-118">Метод передачи данных, в котором между последовательными битами, символами или событиями существует постоянное время.</span><span class="sxs-lookup"><span data-stu-id="74402-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="74402-119">Время достигается общим доступом к одному часам.</span><span class="sxs-lookup"><span data-stu-id="74402-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="74402-120">Каждый конец передачи синхронизируется с использованием часов и сведений, передаваемых вместе с переданными данными.</span><span class="sxs-lookup"><span data-stu-id="74402-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="74402-121">Символы размещаются по времени, а не по начальным и младшим битам.</span><span class="sxs-lookup"><span data-stu-id="74402-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="74402-122">См. раздел [*асинхронные*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="74402-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



