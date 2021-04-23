---
description: Чтобы выбрать сетевой адаптер из предоставляемой таблицы больших двоичных объектов НПП, вызовите функцию Селектнппблобфромтабле.
ms.assetid: e75b6bb7-cf21-4e25-80a5-3b35f7ed0d0e
title: Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0215ca258c02745a7e5b4c285d6bf7df98a49e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683226"
---
# <a name="selecting-a-nic-from-a-supplied-npp-blob-table"></a><span data-ttu-id="87123-103">Выбор сетевой карты из указанной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="87123-103">Selecting a NIC from a Supplied NPP BLOB table</span></span>

<span data-ttu-id="87123-104">Чтобы выбрать сетевой адаптер из предоставляемой таблицы больших двоичных объектов НПП, вызовите функцию [**селектнппблобфромтабле**](selectnppblobfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="87123-104">To select a network interface card (NIC) from a supplied NPP BLOB table, call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function.</span></span> <span data-ttu-id="87123-105">Эта функция использует пользовательский интерфейс сетевой монитор для вывода сетевых карт, представленных в таблице BLOB-объектов, и возвращает большой двоичный объект НПП, представляющий выбранный сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="87123-105">This function uses the Network Monitor UI to display the NICs represented in the BLOB table and returns the NPP BLOB that represents the selected NIC.</span></span>

<span data-ttu-id="87123-106">При вызове функции [**селектнппблобфромтабле**](selectnppblobfromtable.md) появляется диалоговое окно **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="87123-106">When you call the [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) function, the **Select a network** dialog box appears.</span></span> <span data-ttu-id="87123-107">В нем можно просмотреть сведения о НППС, представленных в таблице BLOB-объектов НПП, выбрать конкретный сетевой интерфейс и просмотреть сведения о связанной с ним структуре больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="87123-107">From it, you can view the details of the NPPs represented in the NPP BLOB table, select a specific NIC, and view the details of its associated NPP BLOB structure.</span></span>

<span data-ttu-id="87123-108">На следующем рисунке показаны сетевые карты, представленные в предоставленной таблице больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="87123-108">The following illustration shows the NICs represented in a supplied NPP BLOB table.</span></span>

![Сетевые карты, представленные в предоставленной таблице больших двоичных объектов НПП](images/networkdb2.png)



| <span data-ttu-id="87123-110">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="87123-110">For more information about</span></span>                        | <span data-ttu-id="87123-111">См.</span><span class="sxs-lookup"><span data-stu-id="87123-111">See</span></span>                                                                                                      |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87123-112">Выбор сетевого адаптера, зарегистрированного на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87123-112">Selecting a NIC registered on the local computer.</span></span> | [<span data-ttu-id="87123-113">Выбор зарегистрированного сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="87123-113">How to select a registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="87123-114">Получение таблицы больших двоичных объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="87123-114">Retrieving an NPP BLOB table.</span></span>                     | [<span data-ttu-id="87123-115">Выбор сетевого адаптера из возвращенной таблицы больших двоичных объектов НПП</span><span class="sxs-lookup"><span data-stu-id="87123-115">How to select a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



