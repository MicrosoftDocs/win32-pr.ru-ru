---
description: Фильтр адресов уведомляет драйвер сетевой монитор, чтобы принимать кадры с одним из множества указанных типов MAC-адресов (Ethernet, Token Ring и FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Запись части фильтра АДДРЕССТАБЛЕ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664414"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="b55d3-103">Запись части фильтра АДДРЕССТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="b55d3-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="b55d3-104">Фильтр адресов уведомляет драйвер сетевой монитор, чтобы принимать кадры с одним из множества указанных типов MAC-адресов (Ethernet, Token Ring и FDDI).</span><span class="sxs-lookup"><span data-stu-id="b55d3-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="b55d3-105">Можно указать не более восьми пар адресов.</span><span class="sxs-lookup"><span data-stu-id="b55d3-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="b55d3-106">В паре адресов можно указать источник, назначение, оба значения или ни одного.</span><span class="sxs-lookup"><span data-stu-id="b55d3-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="b55d3-107">Часть адреса фильтра состоит из двух структур: [**аддресстабле**](addresstable.md) и [**аддресспаир**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="b55d3-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="b55d3-108">Если не указать адреса, то все кадры будут проходить фильтр адресов.</span><span class="sxs-lookup"><span data-stu-id="b55d3-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="b55d3-109">Однако если указать какие бы то ни было адреса, то будут переданы только те кадры, которые прошли данный фильтр адресов.</span><span class="sxs-lookup"><span data-stu-id="b55d3-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="b55d3-110">Создание фильтра адресов включает в себя выделение структуры [**аддресстабле**](addresstable.md) и заполнение элементов структуры [**аддресспаир**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="b55d3-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="b55d3-111">**Построение части адреса фильтра записи**</span><span class="sxs-lookup"><span data-stu-id="b55d3-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="b55d3-112">Используйте флаг **каптурефилтер \_ flags \_ Local \_ only** структуры [**каптурефилтер**](capturefilter.md) , чтобы ограничить захват трафика от локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="b55d3-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="b55d3-113">Установка этого флага не приводит к установке сетевого адаптера в неизбирательный режим. файл записи будет записывать только локальный трафик.</span><span class="sxs-lookup"><span data-stu-id="b55d3-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="b55d3-114">Используйте следующий пример кода для определения структуры [**аддресстабле**](addresstable.md) :</span><span class="sxs-lookup"><span data-stu-id="b55d3-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="b55d3-115">Используйте сведения, перечисленные в следующей таблице, чтобы выбрать тип флага [**аддресспаир**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="b55d3-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="b55d3-116">Flag</span><span class="sxs-lookup"><span data-stu-id="b55d3-116">Flag</span></span>                             | <span data-ttu-id="b55d3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b55d3-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="b55d3-118">\_Флаги адреса \_ соответствуют \_ летнему времени</span><span class="sxs-lookup"><span data-stu-id="b55d3-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="b55d3-119">Соответствует адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="b55d3-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="b55d3-120">\_Флаги адреса \_ совпадают с \_ src</span><span class="sxs-lookup"><span data-stu-id="b55d3-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="b55d3-121">Соответствует адресу источника</span><span class="sxs-lookup"><span data-stu-id="b55d3-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="b55d3-122">\_исключаемые флаги адреса \_</span><span class="sxs-lookup"><span data-stu-id="b55d3-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="b55d3-123">Исключает кадр, если этот адрес найден (определенный источник или назначение).</span><span class="sxs-lookup"><span data-stu-id="b55d3-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="b55d3-124">\_флаг адреса \_ адрес \_ группы \_ DST</span><span class="sxs-lookup"><span data-stu-id="b55d3-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="b55d3-125">Соответствует биту группы (адресу назначения) только для сообщений типа Broadcast.</span><span class="sxs-lookup"><span data-stu-id="b55d3-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="b55d3-126">\_Флаги адреса \_ совпадают \_</span><span class="sxs-lookup"><span data-stu-id="b55d3-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="b55d3-127">Совпадает с адресами назначения и источника.</span><span class="sxs-lookup"><span data-stu-id="b55d3-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="b55d3-128">Введите адрес назначения, который оценивается по выбранному флагу [**аддресспаир**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="b55d3-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="b55d3-129">Введите адрес источника, который вычисляется по выбранному флагу [**аддресспаир**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="b55d3-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="b55d3-130">Заполните структуру [**аддресстабле**](addresstable.md) массивом структур [**аддресспаир**](addresspair.md) , которые включают пары адресов, которые проверяет драйвер.</span><span class="sxs-lookup"><span data-stu-id="b55d3-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="b55d3-131">Все пары адресов оцениваются как логический оператор или (АДДРЕССПАИР 1 \| \| аддресспаир 2).</span><span class="sxs-lookup"><span data-stu-id="b55d3-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="b55d3-132">В фильтр записи можно включить не более восьми пар адресов.</span><span class="sxs-lookup"><span data-stu-id="b55d3-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



