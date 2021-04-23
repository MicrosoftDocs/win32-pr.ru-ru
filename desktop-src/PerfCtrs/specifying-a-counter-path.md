---
description: Система использует счетчики для получения данных о производительности.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Указание пути счетчика)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663153"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="0c066-103">Specifying a Counter Path (Указание пути счетчика)</span><span class="sxs-lookup"><span data-stu-id="0c066-103">Specifying a Counter Path</span></span>

<span data-ttu-id="0c066-104">Система использует счетчики для получения данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="0c066-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="0c066-105">Каждый счетчик однозначно идентифицируется по его имени, пути или расположению.</span><span class="sxs-lookup"><span data-stu-id="0c066-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="0c066-106">Синтаксис пути счетчика:</span><span class="sxs-lookup"><span data-stu-id="0c066-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="0c066-107">Элемент Computer указывает имя или IP-адрес компьютера, с которого необходимо запросить данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="0c066-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="0c066-108">Имя компьютера является необязательным, если счетчик находится на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0c066-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="0c066-109">Элемент Перфобжект указывает объект производительности для запроса.</span><span class="sxs-lookup"><span data-stu-id="0c066-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="0c066-110">Объект производительности может быть физическим компонентом, например процессорами, дисками, памятью или системным объектом, например процессами и потоками.</span><span class="sxs-lookup"><span data-stu-id="0c066-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="0c066-111">Каждый системный объект связан с функциональным элементом на компьютере и имеет набор стандартных счетчиков, назначенных ему.</span><span class="sxs-lookup"><span data-stu-id="0c066-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="0c066-112">На каждом компьютере может быть установлен другой набор объектов производительности и счетчиков, поскольку приложения могут устанавливать собственные объекты и счетчики производительности.</span><span class="sxs-lookup"><span data-stu-id="0c066-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="0c066-113">Список объектов производительности и счетчиков, установленных на компьютере, см. в диалоговом окне **Добавление счетчиков** в средстве "производительность" на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0c066-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="0c066-114">Эти объекты также перечислены в диалоговом окне Просмотр PDH (см. раздел [Просмотр счетчиков](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="0c066-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="0c066-115">Список объектов и счетчиков производительности системы см. в разделе [счетчики по объектам](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="0c066-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="0c066-116">Парентинстанце, ObjectInstance и Инстанцеиндекс включены в путь, если может существовать несколько экземпляров объекта.</span><span class="sxs-lookup"><span data-stu-id="0c066-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="0c066-117">Например, процессы и потоки являются несколькими объектами экземпляра, так как одновременно может выполняться несколько процессов или потоков.</span><span class="sxs-lookup"><span data-stu-id="0c066-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="0c066-118">Если объект может иметь более одного экземпляра, то путь к счетчику должен указывать экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="0c066-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="0c066-119">Формат элементов, связанных с экземпляром, зависит от типа объекта.</span><span class="sxs-lookup"><span data-stu-id="0c066-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="0c066-120">Если объект имеет простые экземпляры, то форматом будет только имя экземпляра, заключенное в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="0c066-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="0c066-121">Пример:</span><span class="sxs-lookup"><span data-stu-id="0c066-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="0c066-122">Если экземпляру этого объекта также требуется имя родительского экземпляра, имя родительского экземпляра должно предшествовать экземпляру объекта и быть разделено символом косой черты.</span><span class="sxs-lookup"><span data-stu-id="0c066-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="0c066-123">Например, потоки принадлежат процессам.</span><span class="sxs-lookup"><span data-stu-id="0c066-123">For example, threads belong to processes.</span></span> <span data-ttu-id="0c066-124">При запросе объекта потока необходимо также указать процесс, к которому он принадлежит, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="0c066-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="0c066-125">Если объект имеет несколько экземпляров, имеющих одну и ту же строку имени, их можно индексировать последовательно, указывая индекс экземпляра, префиксом которого является символ решетки.</span><span class="sxs-lookup"><span data-stu-id="0c066-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="0c066-126">Индексы экземпляров основаны на 0.</span><span class="sxs-lookup"><span data-stu-id="0c066-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="0c066-127">Если требуется выполнить запрос к первому экземпляру, не включайте значение \# 0 — просто укажите имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0c066-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="0c066-128">Чтобы указать второй экземпляр, используйте \# 1;, чтобы указать третий экземпляр, используйте \# 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="0c066-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="0c066-129">Пример:</span><span class="sxs-lookup"><span data-stu-id="0c066-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="0c066-130">Элемент Counter указывает счетчик производительности, который необходимо запросить для данного объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="0c066-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="0c066-131">PDH использует следующие специальные символы в пути счетчика.</span><span class="sxs-lookup"><span data-stu-id="0c066-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="0c066-132">Поставщики не должны использовать эти символы в именах.</span><span class="sxs-lookup"><span data-stu-id="0c066-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="0c066-133">Если поставщик использует эти специальные символы, PDH не может проанализировать полный путь к счетчику, чтобы получить имена счетчиков и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="0c066-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="0c066-134">Знак</span><span class="sxs-lookup"><span data-stu-id="0c066-134">Character</span></span> | <span data-ttu-id="0c066-135">Описание</span><span class="sxs-lookup"><span data-stu-id="0c066-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="0c066-136">Универсальный разделитель для Computer, Object и Counter.</span><span class="sxs-lookup"><span data-stu-id="0c066-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="0c066-137">(</span><span class="sxs-lookup"><span data-stu-id="0c066-137">(</span></span>         | <span data-ttu-id="0c066-138">Начало имени экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0c066-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="0c066-139">)</span><span class="sxs-lookup"><span data-stu-id="0c066-139">)</span></span>         | <span data-ttu-id="0c066-140">Конец имени экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0c066-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="0c066-141">Разделяет экземпляр и родительский экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0c066-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="0c066-142">\#n</span><span class="sxs-lookup"><span data-stu-id="0c066-142">\#n</span></span>       | <span data-ttu-id="0c066-143">Определяет конкретное вхождение того же именованного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0c066-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="0c066-144">Подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="0c066-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="0c066-145">В следующих примерах показаны возможные форматы для путей к счетчикам.</span><span class="sxs-lookup"><span data-stu-id="0c066-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="0c066-146">\\\\\\Счетчик объекта "компьютер" (индекс родителя или экземпляра \# ) \\</span><span class="sxs-lookup"><span data-stu-id="0c066-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="0c066-147">\\\\\\Счетчик объекта "компьютер (родительский/экземпляр)" \\</span><span class="sxs-lookup"><span data-stu-id="0c066-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="0c066-148">\\\\\\Счетчик объекта "компьютер ( \# индекс экземпляра)" \\</span><span class="sxs-lookup"><span data-stu-id="0c066-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="0c066-149">\\\\\\Счетчик объекта "компьютер (экземпляр)" \\</span><span class="sxs-lookup"><span data-stu-id="0c066-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="0c066-150">\\\\\\Счетчик объектов "компьютер" \\</span><span class="sxs-lookup"><span data-stu-id="0c066-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="0c066-151">\\Счетчик объектов (индекс родителя или экземпляра \# ) \\</span><span class="sxs-lookup"><span data-stu-id="0c066-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="0c066-152">\\объект (родительский/экземпляр)- \\ Счетчик</span><span class="sxs-lookup"><span data-stu-id="0c066-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="0c066-153">\\Счетчик объекта ( \# индекс экземпляра) \\</span><span class="sxs-lookup"><span data-stu-id="0c066-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="0c066-154">\\Счетчик объекта (экземпляра) \\</span><span class="sxs-lookup"><span data-stu-id="0c066-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="0c066-155">\\\\Счетчик объектов</span><span class="sxs-lookup"><span data-stu-id="0c066-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="0c066-156">Использование подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="0c066-156">Using wildcard characters</span></span>

<span data-ttu-id="0c066-157">Пути счетчиков могут содержать символ-шаблон только для имени экземпляра, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="0c066-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="0c066-158">Чтобы расширить шаблон до списка путей счетчиков, содержащих экземпляры, найденные на компьютере или в файле журнала, вызовите [**пдхекспандвилдкардпас**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="0c066-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
