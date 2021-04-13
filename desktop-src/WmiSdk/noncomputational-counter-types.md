---
description: Невычисляемые типы счетчиков не имеют связанной формулы. Необработанное значение напрямую имеет смысл.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Невычислительные типы счетчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265376"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="70289-104">Невычислительные типы счетчиков</span><span class="sxs-lookup"><span data-stu-id="70289-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="70289-105">Невычисляемые типы счетчиков не имеют связанной формулы.</span><span class="sxs-lookup"><span data-stu-id="70289-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="70289-106">Необработанное значение напрямую имеет смысл.</span><span class="sxs-lookup"><span data-stu-id="70289-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="70289-107">Свойство **филестобеиндексед** в классе [**Win32 \_ перфравдата \_ контентиндекс \_ индексингсервице**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) является примером типа счетчика **\_ счетчика производительности \_ равкаунт** .</span><span class="sxs-lookup"><span data-stu-id="70289-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="70289-108">Он содержит количество файлов, которые не были проиндексированы.</span><span class="sxs-lookup"><span data-stu-id="70289-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="70289-109">Типы счетчиков определяются константой, определенной в Винперф. h, которая находится в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="70289-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="70289-110">В следующей таблице перечислены предоставленные невычислительные типы счетчиков.</span><span class="sxs-lookup"><span data-stu-id="70289-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="70289-111">CounterType</span><span class="sxs-lookup"><span data-stu-id="70289-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="70289-112">Описание</span><span class="sxs-lookup"><span data-stu-id="70289-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70289-113">[Производительность \_ Десятичный \_ текст счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))2816</span><span class="sxs-lookup"><span data-stu-id="70289-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="70289-114">Этот тип счетчика содержит текстовую строку переменной длины в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="70289-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="70289-115">Вычисляемые значения не отображаются.</span><span class="sxs-lookup"><span data-stu-id="70289-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="70289-116">[Производительность \_ Счетчик \_ равкаунт](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))десятичное число 65536</span><span class="sxs-lookup"><span data-stu-id="70289-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="70289-117">Необработанное значение счетчика, которое не требует вычислений, и представляет один пример, который является последним наблюдаемым значением.</span><span class="sxs-lookup"><span data-stu-id="70289-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="70289-118">[Производительность \_ Счетчик \_ крупный \_ равкаунт](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))десятичный 65792</span><span class="sxs-lookup"><span data-stu-id="70289-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="70289-119">То же, что и **\_ Счетчик производительности \_ равкаунт**, но 64-разрядное представление для больших значений.</span><span class="sxs-lookup"><span data-stu-id="70289-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="70289-120">[Производительность \_ Равкаунт СЧЕТЧИКа \_ \_ Шестнадцатеричный](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="70289-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="70289-121">Последнее наблюдаемое значение в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="70289-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="70289-122">Он не отображает среднее значение.</span><span class="sxs-lookup"><span data-stu-id="70289-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="70289-123">[Производительность \_ Счетчик \_ крупный \_ равкаунт \_ шестнадцатеричный](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))десятичный 256</span><span class="sxs-lookup"><span data-stu-id="70289-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="70289-124">То же, что и **\_ Счетчик производительности \_ равкаунт \_ Hex**, но 64-разрядное представление в шестнадцатеричном формате для больших значений.</span><span class="sxs-lookup"><span data-stu-id="70289-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="70289-125">См. также</span><span class="sxs-lookup"><span data-stu-id="70289-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70289-126">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="70289-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

