---
description: При выборе зарегистрированного сетевого адаптера, указанного на локальном компьютере, можно использовать фильтрный большой двоичный объект, чтобы игнорировать сетевые карты, которые вас не интересуют.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Указание фильтра BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682786"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="84335-103">Указание фильтра BLOB</span><span class="sxs-lookup"><span data-stu-id="84335-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="84335-104">При выборе зарегистрированного сетевого адаптера, указанного на локальном компьютере, можно использовать [*фильтрный большой двоичный объект*](f.md) , чтобы игнорировать сетевые карты, которые вас не интересуют.</span><span class="sxs-lookup"><span data-stu-id="84335-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="84335-105">Например, можно ограничить область поиска конкретным типом карты (например, ETHERNET) или определенным MAC-адресом.</span><span class="sxs-lookup"><span data-stu-id="84335-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="84335-106">Во время поиска сетевой карты каждая запись в большом двоичном объекте фильтра должна соответствовать эквивалентной записи в большом двоичном объекте НПП, представляющем сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="84335-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="84335-107">Объекты фильтрации BLOB-объектов также могут быть [*специальными BLOB-объектами*](s.md).</span><span class="sxs-lookup"><span data-stu-id="84335-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="84335-108">Когда вызывается функция [**жетнппблобфромуи**](getnppblobfromui.md) , большой двоичный объект фильтра будет ограничивать сетевые карты, отображаемые в диалоговом окне **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="84335-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="84335-109">При вызове функции [**жетнппблобтабле**](getnppblobtable.md) в большом двоичном объекте фильтра ограничиваются сетевые адаптеры, возвращаемые в таблице больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="84335-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="84335-110">Чтобы использовать фильтр, необходимо создать большой двоичный объект фильтра, задать значения свойств, по которым будет выполняться фильтрация (включая специальные записи больших двоичных объектов), а затем указать фильтр больших двоичных объектов и вызов функции [**жетнппблобтабле**](getnppblobtable.md) или [**жетнппблобфромуи**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="84335-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="84335-111">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="84335-111">For information on</span></span>                                 | <span data-ttu-id="84335-112">См.</span><span class="sxs-lookup"><span data-stu-id="84335-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84335-113">Выбор сетевого адаптера, зарегистрированного на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="84335-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="84335-114">Выбор зарегистрированного сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="84335-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="84335-115">Получение таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="84335-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="84335-116">Выбор сетевой карты из возвращенной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="84335-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



