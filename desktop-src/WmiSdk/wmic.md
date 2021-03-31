---
description: Служебная программа командной строки WMI (WMIC) предоставляет интерфейс командной строки для инструментария WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed46e8aeab24acb44f51099a6e813e921dd77eaa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104273669"
---
# <a name="wmic"></a><span data-ttu-id="83d8c-103">wmic</span><span class="sxs-lookup"><span data-stu-id="83d8c-103">wmic</span></span>

<span data-ttu-id="83d8c-104">Служебная программа командной строки WMI (WMIC) предоставляет интерфейс командной строки для инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="83d8c-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="83d8c-105">WMIC совместим с существующими оболочками и командами служебной программы.</span><span class="sxs-lookup"><span data-stu-id="83d8c-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="83d8c-106">Ниже приведен общий справочный раздел для WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="83d8c-107">Дополнительные сведения и рекомендации по использованию WMIC, включая дополнительные сведения о псевдонимах, глаголах, переключателях и командах, см. в разделе [использование инструментарий управления Windows (WMI) командной строки](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) и [WMIC-take управление WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10))с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="83d8c-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="83d8c-108">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="83d8c-108">Alias</span></span>

<span data-ttu-id="83d8c-109">Псевдоним — это понятное Переименование класса, свойства или метода, который упрощает использование и чтение WMI.</span><span class="sxs-lookup"><span data-stu-id="83d8c-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="83d8c-110">Вы можете определить псевдонимы, доступные для WMIC, с помощью **/?**</span><span class="sxs-lookup"><span data-stu-id="83d8c-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="83d8c-111">.</span><span class="sxs-lookup"><span data-stu-id="83d8c-111">command.</span></span> <span data-ttu-id="83d8c-112">Можно также определить псевдонимы для определенного класса с помощью **<className> /?**</span><span class="sxs-lookup"><span data-stu-id="83d8c-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="83d8c-113">.</span><span class="sxs-lookup"><span data-stu-id="83d8c-113">command.</span></span> <span data-ttu-id="83d8c-114">Дополнительные сведения см. в разделе [псевдонимы WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="83d8c-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="83d8c-115">Коммутатор</span><span class="sxs-lookup"><span data-stu-id="83d8c-115">Switch</span></span>

<span data-ttu-id="83d8c-116">Переключатель — это параметр WMIC, который можно задать глобально или при необходимости.</span><span class="sxs-lookup"><span data-stu-id="83d8c-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="83d8c-117">Список доступных параметров см. в разделе [Параметры WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="83d8c-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="83d8c-118">Команды</span><span class="sxs-lookup"><span data-stu-id="83d8c-118">Verbs</span></span>

<span data-ttu-id="83d8c-119">Чтобы использовать глаголы в WMIC, введите имя псевдонима, а затем команду.</span><span class="sxs-lookup"><span data-stu-id="83d8c-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="83d8c-120">Если псевдоним не поддерживает команду, вы получаете сообщение «поставщик не может выполнить операцию.»</span><span class="sxs-lookup"><span data-stu-id="83d8c-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="83d8c-121">Дополнительные сведения см. в разделе [команды WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="83d8c-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="83d8c-122">Большинство псевдонимов поддерживают следующие команды.</span><span class="sxs-lookup"><span data-stu-id="83d8c-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="83d8c-123"><span id="ASSOC"></span><span id="assoc"></span>ЗАМЫКАЮЩ</span><span class="sxs-lookup"><span data-stu-id="83d8c-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-124">Возвращает результат запроса, в `Associators of (<wmi_object>)` котором *<WMI- \_ объект>* является путем к объектам, возвращаемым командами **пути** или **класса** .</span><span class="sxs-lookup"><span data-stu-id="83d8c-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="83d8c-125">Результаты представляют собой экземпляры, связанные с объектом.</span><span class="sxs-lookup"><span data-stu-id="83d8c-125">The results are instances associated with the object.</span></span> <span data-ttu-id="83d8c-126">Если параметр ASSOC используется с псевдонимом, возвращаются классы с классом, соответствующим псевдониму.</span><span class="sxs-lookup"><span data-stu-id="83d8c-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="83d8c-127">По умолчанию выходные данные возвращаются в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="83d8c-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="83d8c-128">Команда ASSOC имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="83d8c-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="83d8c-129">Параметр</span><span class="sxs-lookup"><span data-stu-id="83d8c-129">Switch</span></span>                         | <span data-ttu-id="83d8c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="83d8c-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d8c-131">/РЕСУЛТКЛАСС:<classname></span><span class="sxs-lookup"><span data-stu-id="83d8c-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="83d8c-132">Возвращенные конечные точки, связанные с исходным объектом, должны принадлежать к указанному классу или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="83d8c-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="83d8c-133">/РЕСУЛТРОЛЕ:<rolename></span><span class="sxs-lookup"><span data-stu-id="83d8c-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="83d8c-134">Возвращенные конечные точки должны играть определенную роль в связях с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="83d8c-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="83d8c-135">/АССОККЛАСС:<assocclass></span><span class="sxs-lookup"><span data-stu-id="83d8c-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="83d8c-136">Возвращенные конечные точки должны быть связаны с источником через указанный класс или один из его производных классов.</span><span class="sxs-lookup"><span data-stu-id="83d8c-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="83d8c-137">Пример: **Assoc для ОС**</span><span class="sxs-lookup"><span data-stu-id="83d8c-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-138"><span id="CALL"></span><span id="call"></span>ОБРАЩЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83d8c-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-139">Выполняет метод.</span><span class="sxs-lookup"><span data-stu-id="83d8c-139">Executes a method.</span></span>

<span data-ttu-id="83d8c-140">Пример: **служба, где Caption = "Telnet", вызов STARTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="83d8c-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="83d8c-141">Чтобы определить методы, доступные для данного класса, используйте **/?**.</span><span class="sxs-lookup"><span data-stu-id="83d8c-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="83d8c-142">Например, **служба, где Caption = "Telnet" Call/?**</span><span class="sxs-lookup"><span data-stu-id="83d8c-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="83d8c-143">Перечисляет доступные функции для класса службы.</span><span class="sxs-lookup"><span data-stu-id="83d8c-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="83d8c-144"><span id="CREATE"></span><span id="create"></span>СОЗДАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83d8c-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-145">Создает новый экземпляр и задает значения свойств.</span><span class="sxs-lookup"><span data-stu-id="83d8c-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="83d8c-146">CREATE не может использоваться для создания нового класса.</span><span class="sxs-lookup"><span data-stu-id="83d8c-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="83d8c-147">Пример: **имя среды Create = "Temp"; ВАРИАБЛЕВАЛУЕ = "создать"**</span><span class="sxs-lookup"><span data-stu-id="83d8c-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-148"><span id="DELETE"></span><span id="delete"></span>УДАЛЕН</span><span class="sxs-lookup"><span data-stu-id="83d8c-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-149">Удаляет текущий экземпляр или набор экземпляров.</span><span class="sxs-lookup"><span data-stu-id="83d8c-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="83d8c-150">DELETE можно использовать для удаления класса.</span><span class="sxs-lookup"><span data-stu-id="83d8c-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="83d8c-151">Пример: **Process, где name = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="83d8c-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-152"><span id="GET"></span><span id="get"></span>Получить</span><span class="sxs-lookup"><span data-stu-id="83d8c-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-153">Получение значений конкретных свойств.</span><span class="sxs-lookup"><span data-stu-id="83d8c-153">Retrieve specific property values.</span></span>

<span data-ttu-id="83d8c-154">GET имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="83d8c-154">GET has the following switches.</span></span>



| <span data-ttu-id="83d8c-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="83d8c-155">Switch</span></span>                               | <span data-ttu-id="83d8c-156">Описание</span><span class="sxs-lookup"><span data-stu-id="83d8c-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d8c-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="83d8c-157">/VALUE</span></span>                               | <span data-ttu-id="83d8c-158">Выходные данные форматируются с каждым значением, перечисленным в отдельной строке, с именем свойства.</span><span class="sxs-lookup"><span data-stu-id="83d8c-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="83d8c-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="83d8c-159">/ALL</span></span>                                 | <span data-ttu-id="83d8c-160">Выходные данные форматируются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="83d8c-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="83d8c-161">Указанный<translation table></span><span class="sxs-lookup"><span data-stu-id="83d8c-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="83d8c-162">Преобразовывать выходные данные с помощью таблицы перевода, именуемой командой.</span><span class="sxs-lookup"><span data-stu-id="83d8c-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="83d8c-163">Таблицы преобразования Басикксмл и "with запятая" включены в WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="83d8c-164">Неделю<interval></span><span class="sxs-lookup"><span data-stu-id="83d8c-164">/EVERY:<interval></span></span>              | <span data-ttu-id="83d8c-165">Повторите команду каждые <interval> секунд.</span><span class="sxs-lookup"><span data-stu-id="83d8c-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="83d8c-166">Формат<format specifier></span><span class="sxs-lookup"><span data-stu-id="83d8c-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="83d8c-167">Задает ключевое слово или имя файла XSL для форматирования данных.</span><span class="sxs-lookup"><span data-stu-id="83d8c-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="83d8c-168">Пример: **имя процесса Get**</span><span class="sxs-lookup"><span data-stu-id="83d8c-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-169"><span id="LIST"></span><span id="list"></span>ЧИСЛ</span><span class="sxs-lookup"><span data-stu-id="83d8c-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-170">Показывает данные.</span><span class="sxs-lookup"><span data-stu-id="83d8c-170">Shows data.</span></span> <span data-ttu-id="83d8c-171">Команда LIST является командой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83d8c-171">LIST is the default verb.</span></span>

<span data-ttu-id="83d8c-172">СПИСОК содержит следующие модификаторам.</span><span class="sxs-lookup"><span data-stu-id="83d8c-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="83d8c-173">Модификаторов</span><span class="sxs-lookup"><span data-stu-id="83d8c-173">Adverb</span></span>   | <span data-ttu-id="83d8c-174">Описание</span><span class="sxs-lookup"><span data-stu-id="83d8c-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="83d8c-175">BRIEF</span><span class="sxs-lookup"><span data-stu-id="83d8c-175">BRIEF</span></span>    | <span data-ttu-id="83d8c-176">Основной набор свойств.</span><span class="sxs-lookup"><span data-stu-id="83d8c-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="83d8c-177">FULL</span><span class="sxs-lookup"><span data-stu-id="83d8c-177">FULL</span></span>     | <span data-ttu-id="83d8c-178">Полный набор свойств.</span><span class="sxs-lookup"><span data-stu-id="83d8c-178">Full set of properties.</span></span> <span data-ttu-id="83d8c-179">Это модификаторов по умолчанию для LIST.</span><span class="sxs-lookup"><span data-stu-id="83d8c-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="83d8c-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="83d8c-180">INSTANCE</span></span> | <span data-ttu-id="83d8c-181">Только пути к экземплярам.</span><span class="sxs-lookup"><span data-stu-id="83d8c-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="83d8c-182">Состояние</span><span class="sxs-lookup"><span data-stu-id="83d8c-182">STATUS</span></span>   | <span data-ttu-id="83d8c-183">Состояние объектов.</span><span class="sxs-lookup"><span data-stu-id="83d8c-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="83d8c-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="83d8c-184">SYSTEM</span></span>   | <span data-ttu-id="83d8c-185">Системные свойства.</span><span class="sxs-lookup"><span data-stu-id="83d8c-185">System properties.</span></span>                                           |



 

<span data-ttu-id="83d8c-186">СПИСОК содержит следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="83d8c-186">LIST has the following switches.</span></span>



| <span data-ttu-id="83d8c-187">Параметр</span><span class="sxs-lookup"><span data-stu-id="83d8c-187">Switch</span></span>                               | <span data-ttu-id="83d8c-188">Описание</span><span class="sxs-lookup"><span data-stu-id="83d8c-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d8c-189">Указанный<translation table></span><span class="sxs-lookup"><span data-stu-id="83d8c-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="83d8c-190">Преобразовывать выходные данные с помощью таблицы перевода, именуемой командой.</span><span class="sxs-lookup"><span data-stu-id="83d8c-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="83d8c-191">Таблицы преобразования Басикксмл и "with запятая" включены в WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="83d8c-192">Неделю<interval></span><span class="sxs-lookup"><span data-stu-id="83d8c-192">/EVERY:<interval></span></span>              | <span data-ttu-id="83d8c-193">Повторите команду каждые <interval> секунд.</span><span class="sxs-lookup"><span data-stu-id="83d8c-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="83d8c-194">Формат<format specifier></span><span class="sxs-lookup"><span data-stu-id="83d8c-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="83d8c-195">Задает ключевое слово или имя файла XSL для форматирования данных.</span><span class="sxs-lookup"><span data-stu-id="83d8c-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="83d8c-196">Пример: **краткий список процессов**</span><span class="sxs-lookup"><span data-stu-id="83d8c-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-197"><span id="SET"></span><span id="set"></span>ПАРАМЕТР</span><span class="sxs-lookup"><span data-stu-id="83d8c-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-198">Присваивает значения свойствам.</span><span class="sxs-lookup"><span data-stu-id="83d8c-198">Assigns values to properties.</span></span> <span data-ttu-id="83d8c-199">Пример: **имя набора окружения = "Temp"**, **ВАРИАБЛЕВАЛУЕ = "New"**</span><span class="sxs-lookup"><span data-stu-id="83d8c-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="83d8c-200">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="83d8c-200">Switches</span></span>

<span data-ttu-id="83d8c-201">Глобальные коммутаторы используются для задания значений по умолчанию для среды WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="83d8c-202">Чтобы просмотреть текущее значение условий, заданных этими коммутаторами, введите команду **context** .</span><span class="sxs-lookup"><span data-stu-id="83d8c-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="83d8c-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="83d8c-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-204">Пространство имен, которое обычно используется псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="83d8c-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="83d8c-205">Значение по умолчанию — root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="83d8c-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="83d8c-206">Пример: **/namespace: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="83d8c-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="83d8c-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-208">Пространство имен WMIC обычно ищет псевдонимы и другие сведения WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="83d8c-209">Пример: **/role: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="83d8c-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="83d8c-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-211">Имена компьютеров, разделенные запятыми.</span><span class="sxs-lookup"><span data-stu-id="83d8c-211">Computer names, comma delimited.</span></span> <span data-ttu-id="83d8c-212">Все команды синхронно выполняются для всех компьютеров, перечисленных в этом значении.</span><span class="sxs-lookup"><span data-stu-id="83d8c-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="83d8c-213">Имена файлов должны иметь префикс &.</span><span class="sxs-lookup"><span data-stu-id="83d8c-213">File names must be prefixed with &.</span></span> <span data-ttu-id="83d8c-214">Имена компьютеров в файле должны быть разделены запятыми или находиться в разных строках.</span><span class="sxs-lookup"><span data-stu-id="83d8c-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/имплевел</span><span class="sxs-lookup"><span data-stu-id="83d8c-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-216">Уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="83d8c-216">Impersonation level.</span></span>

<span data-ttu-id="83d8c-217">Пример: **/имплевел: Anonymous**</span><span class="sxs-lookup"><span data-stu-id="83d8c-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/ауслевел</span><span class="sxs-lookup"><span data-stu-id="83d8c-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-219">Уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="83d8c-219">Authentication level.</span></span>

<span data-ttu-id="83d8c-220">Пример: **/ауслевел: PKT**</span><span class="sxs-lookup"><span data-stu-id="83d8c-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="83d8c-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-222">Языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="83d8c-222">Locale.</span></span>

<span data-ttu-id="83d8c-223">Пример: **/locale: MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="83d8c-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/привилежес</span><span class="sxs-lookup"><span data-stu-id="83d8c-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-225">Включение или отключение всех привилегий.</span><span class="sxs-lookup"><span data-stu-id="83d8c-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="83d8c-226">Пример: **/привилежес: enable** или **/привилежес: Disable**</span><span class="sxs-lookup"><span data-stu-id="83d8c-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="83d8c-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-228">Отображает успешное или неуспешное выполнение всех функций, используемых для выполнения команд WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="83d8c-229">Пример: **/Trace: on** или **/Trace: Off**</span><span class="sxs-lookup"><span data-stu-id="83d8c-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-230"><span id="_RECORD"></span><span id="_record"></span>/рекорд</span><span class="sxs-lookup"><span data-stu-id="83d8c-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-231">Записывает все выходные данные в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="83d8c-231">Records all output to an XML file.</span></span> <span data-ttu-id="83d8c-232">Выходные данные также отображаются в командной строке.</span><span class="sxs-lookup"><span data-stu-id="83d8c-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="83d8c-233">Пример: **/рекорд:** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="83d8c-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/интерактиве</span><span class="sxs-lookup"><span data-stu-id="83d8c-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-235">Как правило, выполняется подтверждение команд DELETE.</span><span class="sxs-lookup"><span data-stu-id="83d8c-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="83d8c-236">Пример: **/интерактиве: on** или **/интерактиве: Off**</span><span class="sxs-lookup"><span data-stu-id="83d8c-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/Фаилфаст **On** \|  \| *тимеаутинмиллисекондс*</span><span class="sxs-lookup"><span data-stu-id="83d8c-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-238">Если на компьютерах/NODE выполняется проверка связи перед отправкой команд WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="83d8c-239">Если компьютер не отвечает, команды WMIC не отправляются.</span><span class="sxs-lookup"><span data-stu-id="83d8c-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="83d8c-240">Пример: "/ФАИЛФАСТ: ON" или "/ФАИЛФАСТ: OFF"</span><span class="sxs-lookup"><span data-stu-id="83d8c-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="83d8c-241">**/ФАИЛФАСТ WMIC: 1000**</span><span class="sxs-lookup"><span data-stu-id="83d8c-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-242"><span id="_USER"></span><span id="_user"></span>WMIC</span><span class="sxs-lookup"><span data-stu-id="83d8c-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-243">Имя пользователя, используемое WMIC при доступе к компьютерам/NODE или компьютерам, указанным в псевдонимах.</span><span class="sxs-lookup"><span data-stu-id="83d8c-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="83d8c-244">Появится запрос на ввод пароля.</span><span class="sxs-lookup"><span data-stu-id="83d8c-244">You are prompted for the password.</span></span> <span data-ttu-id="83d8c-245">Имя пользователя нельзя использовать с локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="83d8c-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="83d8c-246">Пример: **/User:**_jsmith_</span><span class="sxs-lookup"><span data-stu-id="83d8c-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="83d8c-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-248">Пароль, используемый WMIC при доступе к/НПДЕ компьютерам.</span><span class="sxs-lookup"><span data-stu-id="83d8c-248">Password used by WMIC when accessing the /NPDE computers.</span></span> <span data-ttu-id="83d8c-249">Пароль отображается в командной строке.</span><span class="sxs-lookup"><span data-stu-id="83d8c-249">The password is visible at the command line.</span></span>

<span data-ttu-id="83d8c-250">Пример: **/password:**_пароль_</span><span class="sxs-lookup"><span data-stu-id="83d8c-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d8c-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-252">Задает режим для всех перенаправлений вывода.</span><span class="sxs-lookup"><span data-stu-id="83d8c-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="83d8c-253">Выходные данные не отображаются в командной строке, а место назначения удаляется перед началом вывода.</span><span class="sxs-lookup"><span data-stu-id="83d8c-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="83d8c-254">Допустимые значения: STDOUT, CLIPBOARD или имя файла.</span><span class="sxs-lookup"><span data-stu-id="83d8c-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="83d8c-255">Пример: **/OUTPUT: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="83d8c-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="83d8c-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-257">Задает режим для всех перенаправлений вывода.</span><span class="sxs-lookup"><span data-stu-id="83d8c-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="83d8c-258">Выходные данные не отображаются в командной строке, а назначение не удаляется перед началом вывода, а выходные данные добавляются в конец текущего содержимого назначения.</span><span class="sxs-lookup"><span data-stu-id="83d8c-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="83d8c-259">Допустимые значения: STDOUT, CLIPBOARD или имя файла.</span><span class="sxs-lookup"><span data-stu-id="83d8c-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="83d8c-260">Пример: **/append: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="83d8c-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/аггрегате</span><span class="sxs-lookup"><span data-stu-id="83d8c-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-262">Используется с параметром **List** и **Get/евери** .</span><span class="sxs-lookup"><span data-stu-id="83d8c-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="83d8c-263">Если параметр AGGREGATE имеет значение ON, то LIST и GET выводят результаты, когда все компьютеры в/NODE либо отвечают, либо превышено время ожидания. Если параметр AGGREGATE имеет значение OFF, список и получение результатов отображаются сразу после получения.</span><span class="sxs-lookup"><span data-stu-id="83d8c-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="83d8c-264">Пример: **/аггрегате: Off** или **/аггрегате: on**</span><span class="sxs-lookup"><span data-stu-id="83d8c-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="83d8c-265">Команды</span><span class="sxs-lookup"><span data-stu-id="83d8c-265">Commands</span></span>

<span data-ttu-id="83d8c-266">Следующие команды WMIC доступны в любое время.</span><span class="sxs-lookup"><span data-stu-id="83d8c-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="83d8c-267">Дополнительные сведения см. в разделе [команды WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="83d8c-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="83d8c-268"><span id="CLASS"></span><span id="class"></span>СМ</span><span class="sxs-lookup"><span data-stu-id="83d8c-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-269">Переход из режима псевдонима по умолчанию WMIC для прямого доступа к классам в схеме WMI.</span><span class="sxs-lookup"><span data-stu-id="83d8c-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="83d8c-270">Дополнительные сведения о доступных классах WMI см. в разделе [классы WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="83d8c-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="83d8c-271">Пример: **WMIC/OUTPUT: c: \\ClassOutput.htm класс Win32 \_ саунддевице**</span><span class="sxs-lookup"><span data-stu-id="83d8c-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-272"><span id="PATH"></span><span id="path"></span>ПУТЬ</span><span class="sxs-lookup"><span data-stu-id="83d8c-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-273">Переход из режима псевдонима по умолчанию WMIC на доступ к экземплярам в схеме WMI напрямую.</span><span class="sxs-lookup"><span data-stu-id="83d8c-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="83d8c-274">Пример: **WMIC/OUTPUT: c: \\PathOutput.txt путь Win32 \_ саунддевице Get/value**</span><span class="sxs-lookup"><span data-stu-id="83d8c-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-275"><span id="CONTEXT"></span><span id="context"></span>ЛОКАЛЬНОГО</span><span class="sxs-lookup"><span data-stu-id="83d8c-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-276">Отображение текущих значений всех глобальных коммутаторов.</span><span class="sxs-lookup"><span data-stu-id="83d8c-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="83d8c-277">Пример: **контекст WMIC**</span><span class="sxs-lookup"><span data-stu-id="83d8c-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-278"><span id="QUIT"></span><span id="quit"></span>ХВАТИТ</span><span class="sxs-lookup"><span data-stu-id="83d8c-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-279">Выход из WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-279">Exit from WMIC.</span></span>

<span data-ttu-id="83d8c-280">Пример: **WMIC Quit**</span><span class="sxs-lookup"><span data-stu-id="83d8c-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="83d8c-281"><span id="EXIT"></span><span id="exit"></span>ВЫПОЛНЯЕТ</span><span class="sxs-lookup"><span data-stu-id="83d8c-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="83d8c-282">Выход из WMIC.</span><span class="sxs-lookup"><span data-stu-id="83d8c-282">Exit from WMIC.</span></span>

<span data-ttu-id="83d8c-283">Пример: **выход WMIC**</span><span class="sxs-lookup"><span data-stu-id="83d8c-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="83d8c-284">Примеры</span><span class="sxs-lookup"><span data-stu-id="83d8c-284">Examples</span></span>

<span data-ttu-id="83d8c-285">В этом сценарии описывается изменение и обновление IP-адресов, подсетей, шлюза и параметров DNS [с помощью примера WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="83d8c-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="83d8c-286">Требования</span><span class="sxs-lookup"><span data-stu-id="83d8c-286">Requirements</span></span>



| <span data-ttu-id="83d8c-287">Требование</span><span class="sxs-lookup"><span data-stu-id="83d8c-287">Requirement</span></span> | <span data-ttu-id="83d8c-288">Значение</span><span class="sxs-lookup"><span data-stu-id="83d8c-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="83d8c-289">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83d8c-289">Minimum supported client</span></span><br/> | <span data-ttu-id="83d8c-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83d8c-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="83d8c-291">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83d8c-291">Minimum supported server</span></span><br/> | <span data-ttu-id="83d8c-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83d8c-292">Windows Server 2008</span></span><br/> |



 

