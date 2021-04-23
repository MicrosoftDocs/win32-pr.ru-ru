---
title: Устранение неполадок подключения к Интернету
description: В этом сценарии пользователь пытается перейти по адресу www.msn.com с помощью протокола HTTPS, но ему не удается подключиться. Вы можете использовать Netsh и сетевой монитор для получения и просмотра трассировок, чтобы определить причину сбоя подключения.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888148"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="4db01-104">Устранение неполадок подключения к Интернету</span><span class="sxs-lookup"><span data-stu-id="4db01-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="4db01-105">В этом сценарии пользователь пытается перейти по адресу www.msn.com с помощью протокола HTTPS, но ему не удается подключиться.</span><span class="sxs-lookup"><span data-stu-id="4db01-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="4db01-106">Вы можете использовать Netsh и сетевой монитор для получения и просмотра трассировок, чтобы определить причину сбоя подключения.</span><span class="sxs-lookup"><span data-stu-id="4db01-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="4db01-107">Во-первых, можно использовать Netsh для запуска трассировки.</span><span class="sxs-lookup"><span data-stu-id="4db01-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="4db01-108">Введите **команду netsh trace Start сценарий = InternetClient TraceFile = MSN. ETL** запускает трассировку для всех поставщиков, включенных в сценарии InternetClient, сохраняя результаты в файл с именем MSN. ETL.</span><span class="sxs-lookup"><span data-stu-id="4db01-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="4db01-109">После использования веб-браузера для попытки доступа к www.msn.com введите **команду netsh trace остановить** завершается и сопоставляет файл трассировки.</span><span class="sxs-lookup"><span data-stu-id="4db01-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="4db01-110">Затем можно открыть файл MSN. ETL в сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="4db01-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="4db01-111">События группируются по ИДЕНТИФИКАТОРу действия на левой панели.</span><span class="sxs-lookup"><span data-stu-id="4db01-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="4db01-112">С помощью **описания фильтра. Contains ("MSN")** будет показывать только те события, которые содержат строку "MSN" в описании протокола.</span><span class="sxs-lookup"><span data-stu-id="4db01-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![Устранение неполадок подключения к Интернету с помощью сетевого монитора (1)](images/internetclient1.png)

<span data-ttu-id="4db01-114">Затем можно проверить события в сводке кадров, чтобы узнать, какое событие будет иметь соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="4db01-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="4db01-115">Выбрав событие, щелкните правой кнопкой мыши и наведите указатель на пункт найти беседы, а затем щелкните Утевент, чтобы выбрать диалог на уровне Утевент.</span><span class="sxs-lookup"><span data-stu-id="4db01-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![Устранение неполадок подключения к Интернету с помощью сетевого монитора (2)](images/internetclient2.png)

<span data-ttu-id="4db01-117">Затем выделено связанное нормализованное действие на левой панели, в данном случае Утевент ActivityID 397.</span><span class="sxs-lookup"><span data-stu-id="4db01-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![Устранение неполадок подключения к Интернету с помощью сетевого монитора (3)](images/internetclient3.png)

<span data-ttu-id="4db01-119">С помощью сетевой монитор для просмотра и фильтрации данных трассировки количество событий, которые необходимо исследовать, уменьшилось с 1989 до 96.</span><span class="sxs-lookup"><span data-stu-id="4db01-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




