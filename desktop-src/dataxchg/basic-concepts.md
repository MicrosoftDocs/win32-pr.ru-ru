---
title: Основные понятия
description: В этом разделе обсуждаются основные понятия, касающиеся динамического обмена данными.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Платформа динамических данных Exchange (DDE), взаимодействие с сервером клиента
- DDE (платформа динамических данных Exchange), взаимодействие с сервером клиента
- Обмен данными, платформа динамических данных Exchange (DDE)
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Платформа динамических данных Exchange (DDE), клиентские приложения
- DDE (платформа динамических данных Exchange), клиентские приложения
- Платформа динамических данных Exchange (DDE), серверные приложения
- DDE (платформа динамических данных Exchange), серверные приложения
- Платформа динамических данных Exchange (DDE), функции обратного вызова
- DDE (платформа динамических данных Exchange), функции обратного вызова
- Платформа динамических данных Exchange (DDE), транзакции
- DDE (платформа динамических данных Exchange), транзакции
- Платформа динамических данных Exchange (DDE), имена служб
- DDE (платформа динамических данных Exchange), имена служб
- Платформа динамических данных Exchange (DDE), имена элементов
- DDE (платформа динамических данных Exchange), имена элементов
- Платформа динамических данных Exchange (DDE), имена разделов
- DDE (платформа динамических данных Exchange), имена разделов
- Платформа динамических данных Exchange (DDE), системный раздел
- DDE (платформа динамических данных Exchange), системный раздел
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), инициализация
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), инициализация
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), функции обратного вызова
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), функции обратного вызова
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), управление строками
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), управление строками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792090"
---
# <a name="basic-concepts-dde"></a><span data-ttu-id="d54ea-131">Основные понятия (DDE)</span><span class="sxs-lookup"><span data-stu-id="d54ea-131">Basic Concepts (DDE)</span></span>

<span data-ttu-id="d54ea-132">Эти понятия являются ключевыми для понимания платформа динамических данных Exchange (DDE) и платформа динамических данных библиотеки управления Exchange (ДДЕМЛ).</span><span class="sxs-lookup"><span data-stu-id="d54ea-132">These concepts are key to understanding Dynamic Data Exchange (DDE) and the Dynamic Data Exchange Management Library (DDEML).</span></span>

-   [<span data-ttu-id="d54ea-133">Взаимодействие между клиентом и сервером</span><span class="sxs-lookup"><span data-stu-id="d54ea-133">Client and Server Interaction</span></span>](#client-and-server-interaction)
-   [<span data-ttu-id="d54ea-134">Транзакции и функция обратного вызова DDE</span><span class="sxs-lookup"><span data-stu-id="d54ea-134">Transactions and the DDE Callback Function</span></span>](#transactions-and-the-dde-callback-function)
-   [<span data-ttu-id="d54ea-135">Имена служб, имена разделов и имена элементов</span><span class="sxs-lookup"><span data-stu-id="d54ea-135">Service Names, Topic Names, and Item Names</span></span>](#service-names-topic-names-and-item-names)
-   [<span data-ttu-id="d54ea-136">Системный раздел</span><span class="sxs-lookup"><span data-stu-id="d54ea-136">System Topic</span></span>](#system-topic)
-   [<span data-ttu-id="d54ea-137">Инициализация</span><span class="sxs-lookup"><span data-stu-id="d54ea-137">Initialization</span></span>](#initialization)
-   [<span data-ttu-id="d54ea-138">Функция обратного вызова</span><span class="sxs-lookup"><span data-stu-id="d54ea-138">Callback Function</span></span>](#callback-function)
-   [<span data-ttu-id="d54ea-139">Управление строками</span><span class="sxs-lookup"><span data-stu-id="d54ea-139">String Management</span></span>](#string-management)
-   [<span data-ttu-id="d54ea-140">ДДЕМЛ и потоки</span><span class="sxs-lookup"><span data-stu-id="d54ea-140">DDEML and Threads</span></span>](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a><span data-ttu-id="d54ea-141">Взаимодействие между клиентом и сервером</span><span class="sxs-lookup"><span data-stu-id="d54ea-141">Client and Server Interaction</span></span>

<span data-ttu-id="d54ea-142">DDE всегда происходит между клиентским приложением и серверным приложением.</span><span class="sxs-lookup"><span data-stu-id="d54ea-142">DDE always occurs between a client application and a server application.</span></span> <span data-ttu-id="d54ea-143">*Клиентское приложение DDE* инициирует обмен, создавая диалог с сервером для отправки транзакций на сервер.</span><span class="sxs-lookup"><span data-stu-id="d54ea-143">The *DDE client application* initiates the exchange by establishing a conversation with the server to send transactions to the server.</span></span> <span data-ttu-id="d54ea-144">Транзакция — это запрос данных или служб.</span><span class="sxs-lookup"><span data-stu-id="d54ea-144">A transaction is a request for data or services.</span></span> <span data-ttu-id="d54ea-145">*Серверное приложение DDE* отвечает на транзакции, предоставляя клиенту данные или службы.</span><span class="sxs-lookup"><span data-stu-id="d54ea-145">The *DDE server application* responds to transactions by providing data or services to the client.</span></span> <span data-ttu-id="d54ea-146">Например, графическое приложение может содержать линейчатую диаграмму, представляющую квартальную прибыль корпорации, но данные линейчатой диаграммы могут содержаться в приложении для работы с электронными таблицами.</span><span class="sxs-lookup"><span data-stu-id="d54ea-146">For example, a graphics application might contain a bar graph representing a corporation's quarterly profits, but the data for the bar graph might be contained in a spreadsheet application.</span></span> <span data-ttu-id="d54ea-147">Чтобы получить последние данные о прибылях, графическое приложение (клиент) может создать диалог с приложением электронной таблицы (сервер).</span><span class="sxs-lookup"><span data-stu-id="d54ea-147">To obtain the latest profit figures, the graphics application (the client) could establish a conversation with the spreadsheet application (the server).</span></span> <span data-ttu-id="d54ea-148">Графическое приложение может отправить транзакцию в приложение электронной таблицы, запросив последние данные о прибылях.</span><span class="sxs-lookup"><span data-stu-id="d54ea-148">The graphics application could then send a transaction to the spreadsheet application, requesting the latest profit figures.</span></span>

<span data-ttu-id="d54ea-149">Сервер может одновременно иметь много клиентов, а клиент может запрашивать данные с нескольких серверов.</span><span class="sxs-lookup"><span data-stu-id="d54ea-149">A server can have many clients at the same time, and a client can request data from multiple servers.</span></span> <span data-ttu-id="d54ea-150">Приложение также может быть клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="d54ea-150">An application can also be both a client and a server.</span></span> <span data-ttu-id="d54ea-151">Как клиент, так и сервер могут завершить диалог в любое время.</span><span class="sxs-lookup"><span data-stu-id="d54ea-151">Either the client or the server can terminate the conversation at any time.</span></span>

## <a name="transactions-and-the-dde-callback-function"></a><span data-ttu-id="d54ea-152">Транзакции и функция обратного вызова DDE</span><span class="sxs-lookup"><span data-stu-id="d54ea-152">Transactions and the DDE Callback Function</span></span>

<span data-ttu-id="d54ea-153">ДДЕМЛ уведомляет приложение о действии DDE, которое влияет на приложение, отправляя транзакции в функцию обратного вызова DDE приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-153">The DDEML notifies an application about DDE activity that affects the application by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="d54ea-154">*Транзакция DDE* похожа на сообщение — это именованная константа, сопровождающая другие параметры, которые содержат дополнительные сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="d54ea-154">A *DDE transaction* is similar to a message   it is a named constant accompanied by other parameters that contain additional information about the transaction.</span></span>

<span data-ttu-id="d54ea-155">ДДЕМЛ передает транзакцию в определенную приложением функцию обратного вызова DDE, которая выполняет действие, соответствующее типу транзакции.</span><span class="sxs-lookup"><span data-stu-id="d54ea-155">The DDEML passes a transaction to an application-defined DDE callback function that carries out an action appropriate to the type of transaction.</span></span> <span data-ttu-id="d54ea-156">Например, когда клиентское приложение пытается установить диалог с серверным приложением, клиент вызывает функцию [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-156">For example, when a client application attempts to establish a conversation with a server application, the client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span> <span data-ttu-id="d54ea-157">Эта функция заставляет ДДЕМЛ отправить транзакцию [**кстип \_ Connect**](xtyp-connect.md) в функцию обратного вызова DDE сервера.</span><span class="sxs-lookup"><span data-stu-id="d54ea-157">This function causes the DDEML to send an [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="d54ea-158">Функция обратного вызова может разрешить диалог, возвращая **true** в ддемл, или запретить диалог, возвращая **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d54ea-158">The callback function can allow the conversation by returning **TRUE** to the DDEML, or it can deny the conversation by returning **FALSE**.</span></span> <span data-ttu-id="d54ea-159">Подробное описание транзакций см. в разделе [Управление транзакциями](transaction-management.md).</span><span class="sxs-lookup"><span data-stu-id="d54ea-159">For a detailed discussion of transactions, see [Transaction Management](transaction-management.md).</span></span>

## <a name="service-names-topic-names-and-item-names"></a><span data-ttu-id="d54ea-160">Имена служб, имена разделов и имена элементов</span><span class="sxs-lookup"><span data-stu-id="d54ea-160">Service Names, Topic Names, and Item Names</span></span>

<span data-ttu-id="d54ea-161">Сервер DDE использует имя службы иерархии с тремя уровнями (именуемое "имя приложения" в предыдущей документации DDE), имя раздела и имя элемента для уникальной идентификации единицы данных, которые сервер может обменивать во время диалога.</span><span class="sxs-lookup"><span data-stu-id="d54ea-161">A DDE server uses a three-level hierarchy   service name (called "application name" in previous DDE documentation), topic name, and item name   to uniquely identify a unit of data the server can exchange during a conversation.</span></span>

<span data-ttu-id="d54ea-162">*Имя службы* — это строка, на которую реагирует серверное приложение, когда клиент пытается установить диалог с сервером.</span><span class="sxs-lookup"><span data-stu-id="d54ea-162">A *service name* is a string a server application responds to when a client attempts to establish a conversation with the server.</span></span> <span data-ttu-id="d54ea-163">Клиент должен указать это имя службы, чтобы установить диалог с сервером.</span><span class="sxs-lookup"><span data-stu-id="d54ea-163">A client must specify this service name to establish a conversation with the server.</span></span> <span data-ttu-id="d54ea-164">Хотя сервер может отвечать на многие имена служб, большинство серверов реагируют только на одно имя.</span><span class="sxs-lookup"><span data-stu-id="d54ea-164">Although a server can respond to many service names, most servers respond to only one name.</span></span>

<span data-ttu-id="d54ea-165">*Имя раздела* — это строка, идентифицирующая логический контекст данных.</span><span class="sxs-lookup"><span data-stu-id="d54ea-165">A *topic name* is a string that identifies a logical data context.</span></span> <span data-ttu-id="d54ea-166">Для серверов, работающих с файловыми документами, имена разделов обычно являются именами файлов. для других серверов они являются другими строками, зависящими от приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-166">For servers that operate on file-based documents, topic names are typically filenames; for other servers, they are other application-specific strings.</span></span> <span data-ttu-id="d54ea-167">Клиент должен указать имя раздела вместе с именем службы сервера при попытке установить диалог с сервером.</span><span class="sxs-lookup"><span data-stu-id="d54ea-167">A client must specify a topic name along with a server's service name when it attempts to establish a conversation with a server.</span></span>

<span data-ttu-id="d54ea-168">*Имя элемента* — это строка, определяющая единицу данных, которые сервер может передать клиенту во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="d54ea-168">An *item name* is a string that identifies a unit of data a server can pass to a client during a transaction.</span></span> <span data-ttu-id="d54ea-169">Например, имя элемента может обозначать целое число, строку, несколько абзацев текста или точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="d54ea-169">For example, an item name might identify an integer, a string, several paragraphs of text, or a bitmap.</span></span>

<span data-ttu-id="d54ea-170">Имена службы, раздела и элемента позволяют клиенту устанавливать диалог с сервером и принимать данные с сервера.</span><span class="sxs-lookup"><span data-stu-id="d54ea-170">The service, topic, and item names enable the client to establish a conversation with a server and to receive data from the server.</span></span>

## <a name="system-topic"></a><span data-ttu-id="d54ea-171">Системный раздел</span><span class="sxs-lookup"><span data-stu-id="d54ea-171">System Topic</span></span>

<span data-ttu-id="d54ea-172">Раздел System содержит контекст для получения сведений об общем интересе любому клиенту DDE.</span><span class="sxs-lookup"><span data-stu-id="d54ea-172">The System topic provides a context for information of general interest to any DDE client.</span></span> <span data-ttu-id="d54ea-173">Рекомендуется все время, чтобы серверные приложения поддерживали системный раздел.</span><span class="sxs-lookup"><span data-stu-id="d54ea-173">It is recommended that server applications support the System topic at all times.</span></span> <span data-ttu-id="d54ea-174">Системный раздел определен в ДДЕМЛ. Файл заголовка H в виде \_ раздела сзддесис.</span><span class="sxs-lookup"><span data-stu-id="d54ea-174">The System topic is defined in the DDEML.H header file as SZDDESYS\_TOPIC.</span></span>

<span data-ttu-id="d54ea-175">Чтобы определить, какие серверы существуют, и какие типы информации они могут предоставить, клиентское приложение может запросить диалог по системному разделу после запуска, установив для имени устройства **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d54ea-175">To determine which servers are present and the kinds of information they can provide, a client application can request a conversation on the System topic upon starting, setting the device name to **NULL**.</span></span> <span data-ttu-id="d54ea-176">Такие диалоговые окна с подстановочными знаками являются дорогостоящими в плане производительности системы, поэтому их следует свести к минимуму.</span><span class="sxs-lookup"><span data-stu-id="d54ea-176">Such wildcard conversations are costly in terms of system performance, so they should be kept to a minimum.</span></span> <span data-ttu-id="d54ea-177">Дополнительные сведения об инициализации сеансов DDE см. в разделе [Управление диалоговыми](conversation-management.md)окнами.</span><span class="sxs-lookup"><span data-stu-id="d54ea-177">For more information about initiating DDE conversations, see [Conversation Management](conversation-management.md).</span></span>

<span data-ttu-id="d54ea-178">Сервер должен поддерживать следующие имена элементов в системном разделе и имена других элементов, полезных для клиента.</span><span class="sxs-lookup"><span data-stu-id="d54ea-178">A server must support the following item names within the System topic and any other item names that are useful to a client.</span></span>



| <span data-ttu-id="d54ea-179">Элемент</span><span class="sxs-lookup"><span data-stu-id="d54ea-179">Item</span></span>                     | <span data-ttu-id="d54ea-180">Описание</span><span class="sxs-lookup"><span data-stu-id="d54ea-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d54ea-181">СЗДДЕ \_ элемент \_ итемлист</span><span class="sxs-lookup"><span data-stu-id="d54ea-181">SZDDE\_ITEM\_ITEMLIST</span></span>    | <span data-ttu-id="d54ea-182">Список элементов, поддерживаемых в несистемном разделе.</span><span class="sxs-lookup"><span data-stu-id="d54ea-182">A list of the items supported under a non-System topic.</span></span> <span data-ttu-id="d54ea-183">(Этот список может меняться в зависимости от момента и от раздела до раздела).</span><span class="sxs-lookup"><span data-stu-id="d54ea-183">(This list can vary from moment to moment and from topic to topic.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d54ea-184">\_форматы элементов \_ сзддесис</span><span class="sxs-lookup"><span data-stu-id="d54ea-184">SZDDESYS\_ITEM\_FORMATS</span></span>  | <span data-ttu-id="d54ea-185">Разделенный символами табуляцией список строк, представляющих все форматы буфера обмена, потенциально поддерживаемые приложением службы.</span><span class="sxs-lookup"><span data-stu-id="d54ea-185">A tab-delimited list of strings representing all clipboard formats potentially supported by the service application.</span></span> <span data-ttu-id="d54ea-186">Строки, представляющие стандартные форматы буфера обмена, эквивалентны \_ значениям CF с \_ удаленным префиксом "CF".</span><span class="sxs-lookup"><span data-stu-id="d54ea-186">Strings that represent predefined clipboard formats are equivalent to the CF\_ values with the "CF\_" prefix removed.</span></span> <span data-ttu-id="d54ea-187">Например, \_ Формат текста CF представлен строкой Text.</span><span class="sxs-lookup"><span data-stu-id="d54ea-187">For example, the CF\_TEXT format is represented by the string "TEXT".</span></span> <span data-ttu-id="d54ea-188">Эти строки должны быть в верхнем регистре, чтобы их можно было определить как Предопределенные форматы.</span><span class="sxs-lookup"><span data-stu-id="d54ea-188">These strings must be uppercase to further identify them as predefined formats.</span></span> <span data-ttu-id="d54ea-189">Список форматов должен отображаться в порядке с наиболее широкими возможностями в содержимом с минимальными возможностями содержимого.</span><span class="sxs-lookup"><span data-stu-id="d54ea-189">The list of formats must appear in the order of most rich in content to least rich in content.</span></span> <span data-ttu-id="d54ea-190">Дополнительные сведения о форматах буфера обмена и данных для подготовки к просмотру см. в разделе [буфер обмена](clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="d54ea-190">For more information about clipboard formats and rendering data, see [Clipboard](clipboard.md).</span></span><br/> |
| <span data-ttu-id="d54ea-191">\_Справка по элементу сзддесис \_</span><span class="sxs-lookup"><span data-stu-id="d54ea-191">SZDDESYS\_ITEM\_HELP</span></span>     | <span data-ttu-id="d54ea-192">Понятные пользователю сведения об общем интересе.</span><span class="sxs-lookup"><span data-stu-id="d54ea-192">User-readable information of general interest.</span></span> <span data-ttu-id="d54ea-193">Этот элемент должен содержать как минимум сведения об использовании функций DDE серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-193">This item must contain, at a minimum, information on how to use the server application's DDE features.</span></span> <span data-ttu-id="d54ea-194">Эти сведения могут включать, но не ограничиваются, как указывать элементы в разделах, как выполнять строки, которые может выполнять сервер, какие транзакции разрешаются, а также как найти справку по другим системным разделам.</span><span class="sxs-lookup"><span data-stu-id="d54ea-194">This information can include, but is not limited to, how to specify items within topics, what execute strings the server can perform, what poke transactions are allowed, and how to find help on other System topic items.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="d54ea-195">СЗДДЕСИС \_ элемент \_ ртнмсг</span><span class="sxs-lookup"><span data-stu-id="d54ea-195">SZDDESYS\_ITEM\_RTNMSG</span></span>   | <span data-ttu-id="d54ea-196">Поддержка подробных сведений о недавно использованном сообщении [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-196">Supporting detail for the most recently used [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="d54ea-197">Этот элемент полезен в тех случаях, когда требуется более 8 бит возвращаемых данных для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-197">This item is useful when more than 8 bits of application-specific return data are required.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d54ea-198">\_состояние элемента \_ сзддесис</span><span class="sxs-lookup"><span data-stu-id="d54ea-198">SZDDESYS\_ITEM\_STATUS</span></span>   | <span data-ttu-id="d54ea-199">Указывает текущее состояние сервера.</span><span class="sxs-lookup"><span data-stu-id="d54ea-199">An indication of the current status of the server.</span></span> <span data-ttu-id="d54ea-200">Как правило, этот элемент поддерживает только \_ Формат текста CF и содержит строку Ready или Busy.</span><span class="sxs-lookup"><span data-stu-id="d54ea-200">Typically, this item supports only the CF\_TEXT format and contains the Ready or Busy string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d54ea-201">СЗДДЕСИС \_ элемент \_ сиситемс</span><span class="sxs-lookup"><span data-stu-id="d54ea-201">SZDDESYS\_ITEM\_SYSITEMS</span></span> | <span data-ttu-id="d54ea-202">Список элементов, поддерживаемых этим сервером в разделе System.</span><span class="sxs-lookup"><span data-stu-id="d54ea-202">A list of the items supported under the System topic by this server.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d54ea-203">\_статьи об элементах сзддесис \_</span><span class="sxs-lookup"><span data-stu-id="d54ea-203">SZDDESYS\_ITEM\_TOPICS</span></span>   | <span data-ttu-id="d54ea-204">Список разделов, поддерживаемых сервером в текущее время.</span><span class="sxs-lookup"><span data-stu-id="d54ea-204">A list of the topics supported by the server at the current time.</span></span> <span data-ttu-id="d54ea-205">(Этот список может меняться в зависимости от времени.)</span><span class="sxs-lookup"><span data-stu-id="d54ea-205">(This list can vary from moment to moment.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="d54ea-206">Эти имена элементов являются значениями, определенными в ДДЕМЛ. Файл заголовка H.</span><span class="sxs-lookup"><span data-stu-id="d54ea-206">These item names are values defined in the DDEML.H header file.</span></span> <span data-ttu-id="d54ea-207">Чтобы получить дескрипторы строк для этих строк, приложение должно использовать функции управления строками ДДЕМЛ так же, как и для любой другой строки в приложении ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="d54ea-207">To obtain string handles to these strings, an application must use the DDEML string-management functions, just as it would for any other string in a DDEML application.</span></span> <span data-ttu-id="d54ea-208">Дополнительные сведения об управлении строками см. в разделе [Управление строками](#string-management).</span><span class="sxs-lookup"><span data-stu-id="d54ea-208">For more information about managing strings, see [String Management](#string-management).</span></span>

## <a name="initialization"></a><span data-ttu-id="d54ea-209">Инициализация</span><span class="sxs-lookup"><span data-stu-id="d54ea-209">Initialization</span></span>

<span data-ttu-id="d54ea-210">Перед вызовом любой другой функции ДДЕМЛ приложение должно вызвать функцию [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-210">Before calling any other DDEML function, an application must call the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="d54ea-211">**Ддеинитиализе** получает идентификатор экземпляра для приложения, регистрирует функцию обратного вызова DDE приложения в DDE и задает флаги фильтра транзакций для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d54ea-211">**DdeInitialize** obtains an instance identifier for the application, registers the application's DDE callback function with the DDE, and specifies the transaction filter flags for the callback function.</span></span>

<span data-ttu-id="d54ea-212">Каждый экземпляр приложения или библиотеки DLL должен передавать свой идентификатор экземпляра в качестве параметра *идинст* любой другой функции ддемл, которая ее требует.</span><span class="sxs-lookup"><span data-stu-id="d54ea-212">Each instance of an application or a DLL must pass its instance identifier as the *idInst* parameter to any other DDEML function that requires it.</span></span> <span data-ttu-id="d54ea-213">Несколько экземпляров ДДЕМЛ предназначены для поддержки библиотек DLL, которые должны использовать ДДЕМЛ в то же время, когда приложение использует его.</span><span class="sxs-lookup"><span data-stu-id="d54ea-213">The purpose of multiple DDEML instances is to support DLLs that must use the DDEML at the same time an application is using it.</span></span> <span data-ttu-id="d54ea-214">Приложение не должно использовать более одного экземпляра ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="d54ea-214">An application must not use more than one instance of the DDEML.</span></span>

<span data-ttu-id="d54ea-215">*Фильтры транзакций* оптимизируют производительность системы за счет предотвращения передачи нежелательных транзакций в функцию обратного вызова DDE приложения ддемл.</span><span class="sxs-lookup"><span data-stu-id="d54ea-215">*Transaction filters* optimize system performance by preventing the DDEML from passing unwanted transactions to the application's DDE callback function.</span></span> <span data-ttu-id="d54ea-216">Приложение задает фильтры транзакций в параметре уфкмд [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)  .</span><span class="sxs-lookup"><span data-stu-id="d54ea-216">An application sets the transaction filters in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* parameter.</span></span> <span data-ttu-id="d54ea-217">Приложение должно задавать флаг фильтра транзакций для каждого типа транзакции, который не обрабатывается в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d54ea-217">An application must specify a transaction filter flag for each type of transaction that it does not process in its callback function.</span></span> <span data-ttu-id="d54ea-218">Приложение может изменить свои фильтры транзакций при последующем вызове **ддеинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="d54ea-218">An application can change its transaction filters with a subsequent call to **DdeInitialize**.</span></span> <span data-ttu-id="d54ea-219">Дополнительные сведения о транзакциях см. в разделе [Управление транзакциями](transaction-management.md).</span><span class="sxs-lookup"><span data-stu-id="d54ea-219">For more information about transactions, see [Transaction Management](transaction-management.md).</span></span>

<span data-ttu-id="d54ea-220">В следующем примере показано, как инициализировать приложение для использования ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="d54ea-220">The following example shows how to initialize an application to use the DDEML.</span></span>


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



<span data-ttu-id="d54ea-221">Приложение должно вызвать функцию [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) , когда больше не будет использовать ддемл.</span><span class="sxs-lookup"><span data-stu-id="d54ea-221">An application must call the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function when it is no longer going to use the DDEML.</span></span> <span data-ttu-id="d54ea-222">Эта функция завершает все беседы, открытые в настоящее время для приложения, и освобождает ресурсы ДДЕМЛ, выделенные для приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-222">This function terminates any conversations currently open for the application and frees the DDEML resources the system allocated for the application.</span></span>

## <a name="callback-function"></a><span data-ttu-id="d54ea-223">Функция Callback</span><span class="sxs-lookup"><span data-stu-id="d54ea-223">Callback Function</span></span>

<span data-ttu-id="d54ea-224">Приложение, использующее ДДЕМЛ, должно предоставлять функцию обратного вызова, которая обрабатывает события DDE, влияющие на приложение.</span><span class="sxs-lookup"><span data-stu-id="d54ea-224">An application that uses the DDEML must provide a callback function that processes the DDE events affecting the application.</span></span> <span data-ttu-id="d54ea-225">ДДЕМЛ уведомляет приложение о таких событиях, отправляя транзакции в функцию обратного вызова DDE приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-225">The DDEML notifies an application of such events by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="d54ea-226">Транзакции, получаемые функцией обратного вызова, зависят от того, какой фильтр обратного вызова имеет приложение, указанное в [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) , и является ли приложение клиентом, сервером или обоими.</span><span class="sxs-lookup"><span data-stu-id="d54ea-226">The transactions a callback function receives depend on which callback filter flags the application specified in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) and whether the application is a client, a server, or both.</span></span> <span data-ttu-id="d54ea-227">Дополнительные сведения см. в разделе [**ддекаллбакк**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).</span><span class="sxs-lookup"><span data-stu-id="d54ea-227">For more information, please see [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).</span></span>

<span data-ttu-id="d54ea-228">В следующем примере показана общая структура функции обратного вызова для типичного клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="d54ea-228">The following example shows the general structure of a callback function for a typical client application.</span></span>


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



<span data-ttu-id="d54ea-229">Параметр *утипе* указывает тип транзакции, отправляемый функции обратного вызова объектом ддемл.</span><span class="sxs-lookup"><span data-stu-id="d54ea-229">The *uType* parameter specifies the transaction type sent to the callback function by the DDEML.</span></span> <span data-ttu-id="d54ea-230">Значения остальных параметров зависят от типа транзакции.</span><span class="sxs-lookup"><span data-stu-id="d54ea-230">The values of the remaining parameters depend on the transaction type.</span></span> <span data-ttu-id="d54ea-231">Типы транзакций и события, которые их создают, описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="d54ea-231">The transaction types and the events that generate them are described in the following topics.</span></span> <span data-ttu-id="d54ea-232">Подробные сведения о каждом типе транзакции см. в разделе [Управление транзакциями](transaction-management.md).</span><span class="sxs-lookup"><span data-stu-id="d54ea-232">For detailed information about each transaction type, see [Transaction Management](transaction-management.md).</span></span>

## <a name="string-management"></a><span data-ttu-id="d54ea-233">Управление строками</span><span class="sxs-lookup"><span data-stu-id="d54ea-233">String Management</span></span>

<span data-ttu-id="d54ea-234">Для выполнения задачи DDE многим функциям ДДЕМЛ требуется доступ к строкам.</span><span class="sxs-lookup"><span data-stu-id="d54ea-234">To carry out a DDE task, many DDEML functions require access to strings.</span></span> <span data-ttu-id="d54ea-235">Например, клиент должен указать имя службы и имя раздела при вызове функции [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) для запроса диалога с сервером.</span><span class="sxs-lookup"><span data-stu-id="d54ea-235">For example, a client must specify a service name and a topic name when it calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function to request a conversation with a server.</span></span> <span data-ttu-id="d54ea-236">Приложение указывает строку, передавая строковый маркер (ХСЗ), а не указатель в функции ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="d54ea-236">An application specifies a string by passing a string handle (HSZ) rather than a pointer in a DDEML function.</span></span> <span data-ttu-id="d54ea-237">*Строковый обработчик* — это значение **типа DWORD** , присваиваемое системой, которое определяет строку.</span><span class="sxs-lookup"><span data-stu-id="d54ea-237">A *string handle* is a **DWORD** value, assigned by the system, that identifies a string.</span></span>

<span data-ttu-id="d54ea-238">Приложение может получить строковый обработчик для конкретной строки, вызвав функцию [**ддекреатестрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-238">An application can obtain a string handle to a particular string by calling the [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) function.</span></span> <span data-ttu-id="d54ea-239">Эта функция регистрирует строку в системе и возвращает в приложение обработчик строк.</span><span class="sxs-lookup"><span data-stu-id="d54ea-239">This function registers the string with the system and returns a string handle to the application.</span></span> <span data-ttu-id="d54ea-240">Приложение может передать этот обработчик функциям ДДЕМЛ, которые должны обращаться к строке.</span><span class="sxs-lookup"><span data-stu-id="d54ea-240">The application can pass the handle to DDEML functions that must access the string.</span></span> <span data-ttu-id="d54ea-241">Следующий пример получает дескрипторы строк для строки системного раздела и строки имени службы.</span><span class="sxs-lookup"><span data-stu-id="d54ea-241">The following example obtains string handles to the System topic string and the service name string.</span></span>


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



<span data-ttu-id="d54ea-242">Параметр *идинст* в предыдущем примере указывает идентификатор экземпляра, полученный функцией [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-242">The *idInst* parameter in the preceding example specifies the instance identifier obtained by the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="d54ea-243">Функция обратного вызова DDE приложения получает один или несколько дескрипторов строк во время большинства транзакций DDE.</span><span class="sxs-lookup"><span data-stu-id="d54ea-243">An application's DDE callback function receives one or more string handles during most DDE transactions.</span></span> <span data-ttu-id="d54ea-244">Например, сервер получает два дескриптора строки во время транзакции [**\_ запроса кстип**](xtyp-request.md) : одна определяет строку, указывающую имя раздела, а другая определяет строку, указывающую имя элемента.</span><span class="sxs-lookup"><span data-stu-id="d54ea-244">For example, a server receives two string handles during the [**XTYP\_REQUEST**](xtyp-request.md) transaction: one identifies a string specifying a topic name, and the other identifies a string specifying an item name.</span></span> <span data-ttu-id="d54ea-245">Приложение может получить длину строки, которая соответствует строковому маркеру, и скопировать ее в определенный приложением буфер, вызвав функцию [**ддекуеристринг**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d54ea-245">An application can obtain the length of the string that corresponds to a string handle and copy the string to an application-defined buffer by calling the [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) function, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



<span data-ttu-id="d54ea-246">Зависящий от экземпляра обработчик строк не может быть сопоставлен с строковым маркером и строкой.</span><span class="sxs-lookup"><span data-stu-id="d54ea-246">An instance-specific string handle cannot be mapped from string handle to string and back to string handle.</span></span> <span data-ttu-id="d54ea-247">Например, несмотря на то, что [**ддекуеристринг**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) создает строку из дескриптора строки, а затем [**ддекреатестрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) создает строковый дескриптор из этой строки, два дескриптора не совпадают, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d54ea-247">For instance, although [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) creates a string from a string handle and then [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) creates a string handle from that string, the two handles are not the same, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



<span data-ttu-id="d54ea-248">Чтобы сравнить значения двух дескрипторов строк, используйте функцию [**ддекмпстрингхандлес**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-248">To compare the values of two string handles, use the [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) function.</span></span>

<span data-ttu-id="d54ea-249">При возврате функции обратного вызова функция обратного вызова DDE передается в недопустимый строковый маркер.</span><span class="sxs-lookup"><span data-stu-id="d54ea-249">A string handle passed to an application's DDE callback function becomes invalid when the callback function returns.</span></span> <span data-ttu-id="d54ea-250">Приложение может сохранить строковый маркер для использования после возврата функции обратного вызова с помощью функции [**ддекипстрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .</span><span class="sxs-lookup"><span data-stu-id="d54ea-250">An application can save a string handle for use after the callback function returns by using the [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) function.</span></span>

<span data-ttu-id="d54ea-251">Когда приложение вызывает [**ддекреатестрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), система вводит указанную строку в таблицу строк и создает обработчик, который он использует для доступа к строке.</span><span class="sxs-lookup"><span data-stu-id="d54ea-251">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), the system enters the specified string into a string table and generates a handle that it uses to access the string.</span></span> <span data-ttu-id="d54ea-252">Система также поддерживает подсчет использования для каждой строки в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="d54ea-252">The system also maintains a usage count for each string in the string table.</span></span>

<span data-ttu-id="d54ea-253">Когда приложение вызывает [**ддекреатестрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) и указывает строку, которая уже существует в таблице, система увеличивает счетчик использования, а не добавляет еще одно вхождение строки.</span><span class="sxs-lookup"><span data-stu-id="d54ea-253">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) and specifies a string that already exists in the table, the system increments the usage count rather than adding another occurrence of the string.</span></span> <span data-ttu-id="d54ea-254">(Приложение также может увеличить счетчик использования с помощью [**ддекипстрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) Когда приложение вызывает функцию [**ддефристрингхандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , система уменьшает счетчик использования.</span><span class="sxs-lookup"><span data-stu-id="d54ea-254">(An application can also increment the usage count by using [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) When an application calls the [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) function, the system decrements the usage count.</span></span>

<span data-ttu-id="d54ea-255">Строка удаляется из таблицы, если ее значение счетчика использования равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d54ea-255">A string is removed from the table when its usage count equals zero.</span></span> <span data-ttu-id="d54ea-256">Так как несколько приложений могут получить этот обработчик для конкретной строки, приложение не должно освобождать строковый обработчик больше, чем он был создан или удерживает этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="d54ea-256">Because more than one application can obtain the handle to a particular string, an application must not free a string handle more times than it has created or retained the handle.</span></span> <span data-ttu-id="d54ea-257">В противном случае приложение может вызвать удаление строки из таблицы, запрещая другим приложениям доступ к строке.</span><span class="sxs-lookup"><span data-stu-id="d54ea-257">Otherwise, the application can cause the string to be removed from the table, denying other applications access to the string.</span></span>

<span data-ttu-id="d54ea-258">Функции управления строками ДДЕМЛ основаны на диспетчере Atom и имеют те же ограничения по размеру, что и атомы.</span><span class="sxs-lookup"><span data-stu-id="d54ea-258">The DDEML string-management functions are based on the atom manager and are subject to the same size restrictions as are atoms.</span></span>

## <a name="ddeml-and-threads"></a><span data-ttu-id="d54ea-259">ДДЕМЛ и потоки</span><span class="sxs-lookup"><span data-stu-id="d54ea-259">DDEML and Threads</span></span>

<span data-ttu-id="d54ea-260">Функция [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) регистрирует приложение в ддемл, создавая экземпляр ддемл.</span><span class="sxs-lookup"><span data-stu-id="d54ea-260">The [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function registers an application with the DDEML, creating a DDEML instance.</span></span> <span data-ttu-id="d54ea-261">Экземпляр ДДЕМЛ основан на потоке и связан с потоком, который вызвал **ддеинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="d54ea-261">A DDEML instance is thread-based, associated with the thread that called **DdeInitialize**.</span></span>

<span data-ttu-id="d54ea-262">Все вызовы функций ДДЕМЛ для объектов, принадлежащих экземпляру ДДЕМЛ, должны быть сделаны из того же потока, который вызвал [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) для создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d54ea-262">All DDEML function calls for objects belonging to a DDEML instance must be made from the same thread that called [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) to create the instance.</span></span> <span data-ttu-id="d54ea-263">При вызове функции ДДЕМЛ из другого потока функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d54ea-263">If you call a DDEML function from a different thread, the function will fail.</span></span> <span data-ttu-id="d54ea-264">Невозможно получить доступ к беседе ДДЕМЛ из потока, отличного от того, который выделил диалог.</span><span class="sxs-lookup"><span data-stu-id="d54ea-264">You cannot access a DDEML conversation from a thread other than the one that allocated the conversation.</span></span>

 

