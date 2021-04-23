---
description: Для получения данных о производительности используются функции PDH.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Использование функций PDH для использования данных счетчика
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909707"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="958ba-103">Использование функций PDH для использования данных счетчика</span><span class="sxs-lookup"><span data-stu-id="958ba-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="958ba-104">Используйте функции PDH для получения данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="958ba-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="958ba-105">Функции PDH проще в использовании, чем [функции реестра](using-the-registry-functions-to-consume-counter-data.md) , и могут использоваться для доступа к данным счетчика для поставщиков v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="958ba-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="958ba-106">PDH имеет API-интерфейсы для сбора текущих данных о производительности, сохранения данных производительности в файлах журнала и чтения данных из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="958ba-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="958ba-107">При написании приложений OneCore Windows нельзя использовать функции абстрагирования вспомогательного метода для данных производительности.</span><span class="sxs-lookup"><span data-stu-id="958ba-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="958ba-108">Вместо этого используйте [функции-потребители версии PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="958ba-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="958ba-109">PDH — это высокоуровневый API, упрощающий сбор данных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="958ba-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="958ba-110">Она помогает выполнять синтаксический анализ запросов, кэширование метаданных, сопоставление экземпляров между примерами, вычисление форматированных значений из необработанных значений, чтение данных из файлов журнала и сохранение данных в файлах журнала.</span><span class="sxs-lookup"><span data-stu-id="958ba-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="958ba-111">PDH автоматически использует [функции реестра](using-the-registry-functions-to-consume-counter-data.md) при сборе данных от **поставщиков v1** и использует [функции потребителя v2](using-the-perflib-functions-to-consume-counter-data.md) при сборе данных от **поставщиков v2**.</span><span class="sxs-lookup"><span data-stu-id="958ba-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="958ba-112">Чтобы получить данные о производительности с помощью функций PDH, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="958ba-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="958ba-113">Создание запроса</span><span class="sxs-lookup"><span data-stu-id="958ba-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="958ba-114">Добавление счетчиков в запрос</span><span class="sxs-lookup"><span data-stu-id="958ba-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="958ba-115">Получение данных о производительности</span><span class="sxs-lookup"><span data-stu-id="958ba-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="958ba-116">Отображение данных о производительности</span><span class="sxs-lookup"><span data-stu-id="958ba-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="958ba-117">Закрытие запроса</span><span class="sxs-lookup"><span data-stu-id="958ba-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="958ba-118">Данные производительности можно собираются из источников или файлов журналов в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="958ba-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="958ba-119">Дополнительные сведения о записи данных о производительности в файлы журналов см. в разделе [Работа с файлами журналов](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="958ba-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="958ba-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="958ba-120">See also</span></span>

- [<span data-ttu-id="958ba-121">Сбор данных о производительности</span><span class="sxs-lookup"><span data-stu-id="958ba-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="958ba-122">Просмотр счетчиков</span><span class="sxs-lookup"><span data-stu-id="958ba-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="958ba-123">Проверка возвращаемых значений интерфейса PDH</span><span class="sxs-lookup"><span data-stu-id="958ba-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="958ba-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="958ba-124">Examples</span></span>](examples.md)
