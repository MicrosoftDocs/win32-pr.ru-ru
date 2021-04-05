---
description: Таблица Каунтердата содержит по одной строке для каждого счетчика, который собирается в определенный момент времени. Количество этих строк будет большим.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: каунтердата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909744"
---
# <a name="counterdata"></a><span data-ttu-id="ea04f-104">каунтердата</span><span class="sxs-lookup"><span data-stu-id="ea04f-104">CounterData</span></span>

<span data-ttu-id="ea04f-105">Таблица **каунтердата** содержит по одной строке для каждого счетчика, который собирается в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="ea04f-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="ea04f-106">Количество этих строк будет большим.</span><span class="sxs-lookup"><span data-stu-id="ea04f-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="ea04f-107">В таблице **каунтердата** определены следующие поля:</span><span class="sxs-lookup"><span data-stu-id="ea04f-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="ea04f-108">**Идентификатор GUID:** Идентификатор GUID для этого набора данных.</span><span class="sxs-lookup"><span data-stu-id="ea04f-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="ea04f-109">Используйте этот ключ для объединения с таблицей [**дисплайтоид**](displaytoid.md) .</span><span class="sxs-lookup"><span data-stu-id="ea04f-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="ea04f-110">**Каунтерид:** Определяет счетчик.</span><span class="sxs-lookup"><span data-stu-id="ea04f-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="ea04f-111">Используйте этот ключ для объединения с таблицей [**каунтердетаилс**](counterdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="ea04f-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="ea04f-112">**Рекординдекс:** Пример индекса для указанного идентификатора счетчика и GUID коллекции.</span><span class="sxs-lookup"><span data-stu-id="ea04f-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="ea04f-113">Значение увеличивается для каждого последующего образца в этом файле журнала.</span><span class="sxs-lookup"><span data-stu-id="ea04f-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="ea04f-114">**Каунтердатетиме:** Время запуска коллекции (в формате UTC).</span><span class="sxs-lookup"><span data-stu-id="ea04f-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="ea04f-115">**CounterValue:** Отформатированное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="ea04f-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="ea04f-116">Это значение может быть нулевым для первой записи, если счетчику требуется два образца для расчета отображаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ea04f-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="ea04f-117">**Фирствалуеа:** Объедините это 32-разрядное значение со значением **фирствалуеб** , чтобы создать элемент **Фирствалуе** [**\_ \_ счетчика PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="ea04f-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="ea04f-118">**Фирствалуеа** содержит младшие биты.</span><span class="sxs-lookup"><span data-stu-id="ea04f-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="ea04f-119">**Фирствалуеб:** Объедините это 32-разрядное значение со значением **фирствалуеа** , чтобы создать элемент **Фирствалуе** [**\_ \_ счетчика PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="ea04f-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="ea04f-120">**Фирствалуеб** содержит старшие биты.</span><span class="sxs-lookup"><span data-stu-id="ea04f-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="ea04f-121">**Секондвалуеа:** Объедините это 32-разрядное значение со значением **секондвалуеб** , чтобы создать элемент **SecondValue** [**\_ \_ счетчика PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="ea04f-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="ea04f-122">**Секондвалуеа** содержит младшие биты.</span><span class="sxs-lookup"><span data-stu-id="ea04f-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="ea04f-123">**Секондвалуеб:** Объедините это 32-разрядное значение со значением **секондвалуеа** , чтобы создать элемент **SecondValue** [**\_ \_ счетчика PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="ea04f-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="ea04f-124">**Секондвалуеб** содержит старшие биты.</span><span class="sxs-lookup"><span data-stu-id="ea04f-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="ea04f-125">Поля **GUID**, **каунтерид** и **рекординдекс** составляют первичный ключ для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="ea04f-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



