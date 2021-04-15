---
description: Выходные функции отладки
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Выходные функции отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655613"
---
# <a name="debug-output-functions"></a><span data-ttu-id="55d9a-103">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="55d9a-103">Debug Output Functions</span></span>

<span data-ttu-id="55d9a-104">[Базовые классы DirectShow](directshow-base-classes.md) предоставляют несколько макросов для отображения отладочной информации.</span><span class="sxs-lookup"><span data-stu-id="55d9a-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="55d9a-105">Функция</span><span class="sxs-lookup"><span data-stu-id="55d9a-105">Function</span></span>                                               | <span data-ttu-id="55d9a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="55d9a-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55d9a-107">**дбгчеккмодулелевел**</span><span class="sxs-lookup"><span data-stu-id="55d9a-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="55d9a-108">Проверяет, включено ли ведение журнала для заданных типов сообщений и уровней.</span><span class="sxs-lookup"><span data-stu-id="55d9a-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="55d9a-109">**дбгдумпобжектрегистер**</span><span class="sxs-lookup"><span data-stu-id="55d9a-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="55d9a-110">Отображает сведения об активных объектах.</span><span class="sxs-lookup"><span data-stu-id="55d9a-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="55d9a-111">**дбгинитиалисе**</span><span class="sxs-lookup"><span data-stu-id="55d9a-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="55d9a-112">Инициализирует библиотеку отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="55d9a-113">**дбглог**</span><span class="sxs-lookup"><span data-stu-id="55d9a-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="55d9a-114">Отправляет строку в расположение выходных данных отладки, если ведение журнала включено для указанного типа и уровня.</span><span class="sxs-lookup"><span data-stu-id="55d9a-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="55d9a-115">**дбгаутстринг**</span><span class="sxs-lookup"><span data-stu-id="55d9a-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="55d9a-116">Отправляет строку в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="55d9a-117">**дбгсетмодулелевел**</span><span class="sxs-lookup"><span data-stu-id="55d9a-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="55d9a-118">Задает уровень ведения журнала для одного или нескольких типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="55d9a-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="55d9a-119">**дбгтерминате**</span><span class="sxs-lookup"><span data-stu-id="55d9a-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="55d9a-120">Очищает библиотеку отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="55d9a-121">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="55d9a-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="55d9a-122">Отправляет сведения о типе мультимедиа в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="55d9a-123">**думпграф**</span><span class="sxs-lookup"><span data-stu-id="55d9a-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="55d9a-124">Отправляет сведения о графе фильтра в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="55d9a-125">**гуиднамес**</span><span class="sxs-lookup"><span data-stu-id="55d9a-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="55d9a-126">Глобальный массив, содержащий строки, представляющие идентификаторы GUID, определенные в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="55d9a-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="55d9a-127">**БЕЗЫМЯН**</span><span class="sxs-lookup"><span data-stu-id="55d9a-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="55d9a-128">Создает строку только для отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="55d9a-129">**МЕТИМ**</span><span class="sxs-lookup"><span data-stu-id="55d9a-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="55d9a-130">Отправляет строку в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="55d9a-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="55d9a-131">**Вам**</span><span class="sxs-lookup"><span data-stu-id="55d9a-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="55d9a-132">Создает напоминание во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="55d9a-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="55d9a-133">**Разделы реестра**</span><span class="sxs-lookup"><span data-stu-id="55d9a-133">**Registry Keys**</span></span>

<span data-ttu-id="55d9a-134">В функции выходных данных отладки в DirectShow используется набор разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="55d9a-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="55d9a-135">Расположение этих разделов реестра зависит от версии Windows.</span><span class="sxs-lookup"><span data-stu-id="55d9a-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="55d9a-136">*До выхода Windows Vista* ключи отладки расположены по следующему пути:</span><span class="sxs-lookup"><span data-stu-id="55d9a-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="55d9a-137">**HKey \_ \_** \\  \\ **Отладка** по локального компьютера</span><span class="sxs-lookup"><span data-stu-id="55d9a-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="55d9a-138">В Windows Vista и более поздних версиях они расположены по следующему пути:</span><span class="sxs-lookup"><span data-stu-id="55d9a-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="55d9a-139">**HKey \_ \_** \\  \\  \\  \\ **Отладка** Microsoft DirectShow по локальному компьютеру</span><span class="sxs-lookup"><span data-stu-id="55d9a-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="55d9a-140">Для фильтров сторонних производителей расположение зависит от того, какая версия [базовых классов DirectShow](directshow-base-classes.md) использовалась для построения фильтра.</span><span class="sxs-lookup"><span data-stu-id="55d9a-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="55d9a-141">Версия, входящая в Windows SDK для Windows Vista, использует более новый путь.</span><span class="sxs-lookup"><span data-stu-id="55d9a-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="55d9a-142">В предыдущих версиях использовался старый путь.</span><span class="sxs-lookup"><span data-stu-id="55d9a-142">Previous versions used the older path.</span></span>

<span data-ttu-id="55d9a-143">В следующих комментариях метка *<DebugRoot>* используется для обозначения этих двух путей.</span><span class="sxs-lookup"><span data-stu-id="55d9a-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="55d9a-144">Замените правильный путь в зависимости от версии Windows или версии базовых классов.</span><span class="sxs-lookup"><span data-stu-id="55d9a-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="55d9a-145">**Ведение журнала отладки**</span><span class="sxs-lookup"><span data-stu-id="55d9a-145">**Debug Logging**</span></span>

<span data-ttu-id="55d9a-146">DirectShow определяет несколько типов сообщений, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55d9a-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="55d9a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="55d9a-147">Value</span></span>                   | <span data-ttu-id="55d9a-148">Описание</span><span class="sxs-lookup"><span data-stu-id="55d9a-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="55d9a-149">\_Ошибка журнала</span><span class="sxs-lookup"><span data-stu-id="55d9a-149">LOG\_ERROR</span></span>              | <span data-ttu-id="55d9a-150">Уведомление об ошибке.</span><span class="sxs-lookup"><span data-stu-id="55d9a-150">Error notification.</span></span>                                     |
| <span data-ttu-id="55d9a-151">\_Блокировка журнала</span><span class="sxs-lookup"><span data-stu-id="55d9a-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="55d9a-152">Блокировка и разблокировка критических разделов.</span><span class="sxs-lookup"><span data-stu-id="55d9a-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="55d9a-153">\_память журнала</span><span class="sxs-lookup"><span data-stu-id="55d9a-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="55d9a-154">Выделение памяти, создание и уничтожение объектов.</span><span class="sxs-lookup"><span data-stu-id="55d9a-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="55d9a-155">время ведения журнала \_</span><span class="sxs-lookup"><span data-stu-id="55d9a-155">LOG\_TIMING</span></span>             | <span data-ttu-id="55d9a-156">Измерения времени и производительности.</span><span class="sxs-lookup"><span data-stu-id="55d9a-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="55d9a-157">\_Трассировка журнала</span><span class="sxs-lookup"><span data-stu-id="55d9a-157">LOG\_TRACE</span></span>              | <span data-ttu-id="55d9a-158">Общая трассировка вызовов.</span><span class="sxs-lookup"><span data-stu-id="55d9a-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="55d9a-159">CUSTOM1 через CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="55d9a-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="55d9a-160">Доступно для настраиваемых сообщений отладки</span><span class="sxs-lookup"><span data-stu-id="55d9a-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="55d9a-161">Каждая из функций ведения журнала отладки DirectShow указывает тип сообщения и уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="55d9a-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="55d9a-162">Сообщение отладки отображается только в том случае, если текущий уровень отладки для этого типа сообщений равен уровню, указанному в функции ведения журнала, или больше него.</span><span class="sxs-lookup"><span data-stu-id="55d9a-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="55d9a-163">В противном случае сообщение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="55d9a-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="55d9a-164">Например, следующий код выводит строку "это сообщение отладки", если \_ уровень трассировки журнала равен 3 или выше:</span><span class="sxs-lookup"><span data-stu-id="55d9a-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="55d9a-165">Каждый модуль может устанавливать собственный уровень отладки для каждого типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="55d9a-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="55d9a-166">( *Модуль* — это библиотека DLL или исполняемый файл, который можно загрузить с помощью функции **LoadLibrary** .) Уровни отладки модуля отображаются в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="55d9a-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="55d9a-167">**HKEY \_ локальный \_ компьютер**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="55d9a-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="55d9a-168">где *<Message Type>* — это тип сообщения минус начальный "журнал \_ ", например **Блокировка** сообщений о \_ блокировке журнала.</span><span class="sxs-lookup"><span data-stu-id="55d9a-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="55d9a-169">При загрузке модуля библиотека отладки находит в реестре уровни ведения журнала модуля.</span><span class="sxs-lookup"><span data-stu-id="55d9a-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="55d9a-170">Если разделы реестра не существуют, Библиотека отладки создаст их.</span><span class="sxs-lookup"><span data-stu-id="55d9a-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="55d9a-171">Модуль также может задавать собственные уровни во время выполнения с помощью функции [**дбгсетмодулелевел**](dbgsetmodulelevel.md) .</span><span class="sxs-lookup"><span data-stu-id="55d9a-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="55d9a-172">Чтобы отправить сообщение в выходные данные отладки, вызовите макрос [**дбглог**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="55d9a-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="55d9a-173">В следующем примере создается сообщение уровня 3 типа \_ Трассировка журнала:</span><span class="sxs-lookup"><span data-stu-id="55d9a-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="55d9a-174">Кроме того, можно указать глобальные уровни ведения журнала с помощью следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="55d9a-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="55d9a-175">Отладочная библиотека использует уровень выше, глобальный уровень или уровень модуля.</span><span class="sxs-lookup"><span data-stu-id="55d9a-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="55d9a-176">**Расположение выходных данных отладки**</span><span class="sxs-lookup"><span data-stu-id="55d9a-176">**Debug Output Location**</span></span>

<span data-ttu-id="55d9a-177">Расположение выходных данных отладки определяется другим ключом реестра:</span><span class="sxs-lookup"><span data-stu-id="55d9a-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="55d9a-178">**HKey \_ \_** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **Логтофиле** локального компьютера</span><span class="sxs-lookup"><span data-stu-id="55d9a-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="55d9a-179">Если значение этого параметра равно `Console` , выходные данные попадают в окно консоли.</span><span class="sxs-lookup"><span data-stu-id="55d9a-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="55d9a-180">Если значение равно `Deb` ,, `Debug` или является `Debugger` пустой строкой, выходные данные попадают в окно отладчика.</span><span class="sxs-lookup"><span data-stu-id="55d9a-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="55d9a-181">В противном случае выходные данные записываются в файл, указанный в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="55d9a-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="55d9a-182">Прежде чем исполняемый файл использует библиотеку отладки DirectShow, он должен вызвать функцию [**дбгинитиалисе**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="55d9a-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="55d9a-183">После этого он должен вызвать функцию [**дбгтерминате**](dbgterminate.md) .</span><span class="sxs-lookup"><span data-stu-id="55d9a-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="55d9a-184">Библиотекам DLL не требуется вызывать эти функции, так как точка входа библиотеки DLL (определенная в библиотеке базовых классов) вызывает их автоматически.</span><span class="sxs-lookup"><span data-stu-id="55d9a-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55d9a-185">См. также</span><span class="sxs-lookup"><span data-stu-id="55d9a-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d9a-186">Отладка служебных программ</span><span class="sxs-lookup"><span data-stu-id="55d9a-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



