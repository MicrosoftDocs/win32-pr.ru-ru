---
description: Сетевой монитор предоставляет три функции для выбора сетевого адаптера. Эти функции предоставляют три способа перечисления набора сетевых карт и выбора того, который вы хотите использовать. Эти функции перечислены в следующей таблице.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Выбор сетевой карты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156038"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="ce4ca-105">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="ce4ca-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="ce4ca-106">Сетевой монитор предоставляет три функции для выбора сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="ce4ca-107">Эти функции предоставляют три способа перечисления набора сетевых карт и выбора того, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="ce4ca-108">Эти функции перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-108">The following table lists these functions.</span></span>



| <span data-ttu-id="ce4ca-109">Функция</span><span class="sxs-lookup"><span data-stu-id="ce4ca-109">Function</span></span>                                                 | <span data-ttu-id="ce4ca-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ce4ca-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce4ca-111">**жетнппблобфромуи**</span><span class="sxs-lookup"><span data-stu-id="ce4ca-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="ce4ca-112">Использует пользовательский интерфейс сетевой монитор для вывода зарегистрированных сетевых карт и возвращает большой двоичный объект НПП, представляющий интересующую вас сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="ce4ca-113">**жетнппблобтабле**</span><span class="sxs-lookup"><span data-stu-id="ce4ca-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="ce4ca-114">Возвращает таблицу больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-114">Returns a BLOB table.</span></span> <span data-ttu-id="ce4ca-115">Приложение должно перечислить таблицу и выбрать большой двоичный объект НПП.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="ce4ca-116">**селектнппблобфромтабле**</span><span class="sxs-lookup"><span data-stu-id="ce4ca-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="ce4ca-117">Использует интерфейс сетевой монитор для вывода предоставляемых BLOB-объектов НПП и возвращает большой двоичный объект НПП, представляющий интересующую вас сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="ce4ca-118">Каждая сетевая карта представлена НПП большим двоичным объектом (BLOB).</span><span class="sxs-lookup"><span data-stu-id="ce4ca-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="ce4ca-119">Эти функции могут возвращать один большой двоичный объект НПП, зарегистрированный на компьютере, один большой двоичный объект НПП из указанной таблицы НПП BLOB или таблицу НПП больших двоичных объектов, которую вызывающий объект должен затем использовать для выбора определенного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="ce4ca-120">В первых двух случаях при выборе из зарегистрированных сетевых адаптеров или из указанной таблицы НПП BLOB в пользовательском интерфейсе сетевой монитор отображаются сетевые карты, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="ce4ca-121">Сетевой монитор использует функцию, называемую НПП Finder для перечисления сетевых адаптеров, зарегистрированных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="ce4ca-122">НПП Finder является компонентом Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="ce4ca-123">Сведения о</span><span class="sxs-lookup"><span data-stu-id="ce4ca-123">For information about</span></span>                            | <span data-ttu-id="ce4ca-124">См.</span><span class="sxs-lookup"><span data-stu-id="ce4ca-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4ca-125">Выбор сетевого адаптера, зарегистрированного на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="ce4ca-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="ce4ca-126">Выбор зарегистрированного сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="ce4ca-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="ce4ca-127">Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="ce4ca-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="ce4ca-128">Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="ce4ca-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="ce4ca-129">Получение таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="ce4ca-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="ce4ca-130">Выбор сетевой карты из возвращенной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="ce4ca-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



