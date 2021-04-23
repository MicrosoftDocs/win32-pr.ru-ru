---
description: Чтобы выбрать один из сетевых адаптеров, зарегистрированных на локальном компьютере, вызовите функцию Жетнппблобфромуи.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Выбор зарегистрированного сетевого адаптера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673545"
---
# <a name="selecting-a-registered-nic"></a><span data-ttu-id="a6584-103">Выбор зарегистрированного сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="a6584-103">Selecting a Registered NIC</span></span>

<span data-ttu-id="a6584-104">Чтобы выбрать один из сетевых адаптеров, зарегистрированных на локальном компьютере, вызовите функцию [**жетнппблобфромуи**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="a6584-104">To select one of the NICs registered on the local computer, call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span> <span data-ttu-id="a6584-105">Эта функция использует пользовательский интерфейс сетевой монитор для вывода зарегистрированных сетевых карт и возвращает большой двоичный объект НПП, представляющий выбранный сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="a6584-105">This function uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you select.</span></span> <span data-ttu-id="a6584-106">Вы можете отобразить все сетевые карты, зарегистрированные на локальном компьютере, или небольшой набор отфильтрованных сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="a6584-106">You can display all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="a6584-107">Чтобы отфильтровать отображаемые сетевые карты, при вызове укажите [*большой двоичный объект фильтра*](f.md) .</span><span class="sxs-lookup"><span data-stu-id="a6584-107">To filter the displayed NICs, provide a [*filter BLOB*](f.md) when the call is made.</span></span>

> [!Note]  
> <span data-ttu-id="a6584-108">Когда вызывается функция [**жетнппблобфромуи**](getnppblobfromui.md) , [*НПП Finder*](n.md) взаимодействует с библиотеками DLL НПП, чтобы получить структуры больших двоичных объектов НПП, представляющие зарегистрированные сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="a6584-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the [*NPP Finder*](n.md) communicates with the NPP DLLs to obtain the NPP BLOB structures that represent the registered NICs.</span></span> <span data-ttu-id="a6584-109">Дополнительные сведения и процедура непосредственного использования пользовательского интерфейса сетевой монитор см. в разделе «Выбор сети» в справке сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a6584-109">For more information, and a procedure about how to use the Network Monitor UI directly, see the "Select a Network Dialog Box" topic in the Network Monitor online help.</span></span>

 

<span data-ttu-id="a6584-110">При вызове функции [**жетнппблобфромуи**](getnppblobfromui.md) появляется диалоговое окно **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="a6584-110">When you call the [**GetNPPBlobFromUI**](getnppblobfromui.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="a6584-111">В нем можно просмотреть сведения о НППС, зарегистрированном на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a6584-111">From it, you can view the details of the NPPs registered on the local computer.</span></span> <span data-ttu-id="a6584-112">Эти сведения включают как локальные НППС, так и удаленный НППС.</span><span class="sxs-lookup"><span data-stu-id="a6584-112">This information includes both local NPPs and remote NPPs.</span></span> <span data-ttu-id="a6584-113">В диалоговом окне можно выбрать конкретный сетевой адаптер и просмотреть сведения о связанной с ним структуре больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="a6584-113">From the dialog box, you can select a specific NIC and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="a6584-114">На следующем рисунке показаны типичные параметры НПП NDIS, предоставляемые сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a6584-114">The following illustration shows typical settings of an NDIS NPP supplied by Network Monitor.</span></span>

![стандартные параметры NDIS НПП, предоставленные сетевым монитором](images/networkdb.png)

<span data-ttu-id="a6584-116">В следующей таблице перечислены разделы, в которых описываются методы выбора сетевых карт.</span><span class="sxs-lookup"><span data-stu-id="a6584-116">The following table lists topics that describe each NIC selection method.</span></span>



| <span data-ttu-id="a6584-117">Сведения о</span><span class="sxs-lookup"><span data-stu-id="a6584-117">For information about</span></span>                                                                          | <span data-ttu-id="a6584-118">См.</span><span class="sxs-lookup"><span data-stu-id="a6584-118">See</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6584-119">Указание фильтра, ограничивающего сетевые карты, отображаемые в диалоговом окне **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="a6584-119">How to specify a filter that limits the NICs displayed in the **Select a network** dialog box.</span></span> | [<span data-ttu-id="a6584-120">Указание фильтра BLOB</span><span class="sxs-lookup"><span data-stu-id="a6584-120">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="a6584-121">Как выбрать сетевой адаптер, вызвав функцию [**жетнппблобфромуи**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="a6584-121">How to select a NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>      | [<span data-ttu-id="a6584-122">Выбор сетевого адаптера с помощью Жетнппблобфромуи</span><span class="sxs-lookup"><span data-stu-id="a6584-122">Selecting a NIC using GetNPPBlobFromUI</span></span>](getnppblobfromui.md)                                       |
| <span data-ttu-id="a6584-123">Как выбрать сетевой адаптер из указанной таблицы больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="a6584-123">How to select a NIC from a supplied NPP BLOB table.</span></span>                                            | [<span data-ttu-id="a6584-124">Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="a6584-124">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



