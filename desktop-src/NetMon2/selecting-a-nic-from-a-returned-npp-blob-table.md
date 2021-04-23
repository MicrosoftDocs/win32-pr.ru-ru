---
description: Чтобы выбрать сетевую карту из таблицы больших двоичных объектов НПП, возвращенной сетевой монитор, вызовите функцию Жетнппблобтабле. Эта функция возвращает таблицу больших двоичных объектов НПП, которую затем можно перечислить с помощью приложения, чтобы выбрать интересующую вас сетевую карту.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Выбор сетевой карты из возвращенной таблицы больших двоичных объектов НПП
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909803"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="42bec-104">Выбор сетевой карты из возвращенной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="42bec-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="42bec-105">Чтобы выбрать сетевую карту из таблицы больших двоичных объектов НПП, возвращенной сетевой монитор, вызовите функцию [**жетнппблобтабле**](getnppblobtable.md) .</span><span class="sxs-lookup"><span data-stu-id="42bec-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="42bec-106">Эта функция возвращает таблицу больших двоичных объектов НПП, которую затем можно перечислить с помощью приложения, чтобы выбрать интересующую вас сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="42bec-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="42bec-107">При вызове этой функции вы можете вернуть либо таблицу больших двоичных объектов всех сетевых адаптеров, зарегистрированных на локальном компьютере, либо небольшой набор фильтруемых сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="42bec-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="42bec-108">Чтобы отфильтровать возвращаемые сетевые карты, при вызове можно указать [*Фильтр большого двоичного объекта*](f.md) .</span><span class="sxs-lookup"><span data-stu-id="42bec-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="42bec-109">Сведения о</span><span class="sxs-lookup"><span data-stu-id="42bec-109">For information about</span></span>                                                       | <span data-ttu-id="42bec-110">См.</span><span class="sxs-lookup"><span data-stu-id="42bec-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bec-111">Как указать фильтр, ограничивающий сетевые адаптеры, возвращаемые в таблице больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="42bec-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="42bec-112">Указание фильтра BLOB</span><span class="sxs-lookup"><span data-stu-id="42bec-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="42bec-113">Как выбрать сетевой адаптер, зарегистрированный на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="42bec-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="42bec-114">Выбор зарегистрированного сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="42bec-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="42bec-115">Выбор сетевого адаптера из указанной таблицы BLOB-объектов НПП</span><span class="sxs-lookup"><span data-stu-id="42bec-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="42bec-116">Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="42bec-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



