---
title: Устранение неполадок беспроводных подключений LAN
description: В этом сценарии пользователь пытается подключиться к беспроводной локальной сети, но не может подключиться. Вы можете использовать Netsh и сетевой монитор для получения и просмотра трассировок, чтобы определить причину сбоя подключения.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068447"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="423e7-104">Устранение неполадок беспроводных подключений LAN</span><span class="sxs-lookup"><span data-stu-id="423e7-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="423e7-105">В этом сценарии пользователь пытается подключиться к беспроводной локальной сети, но не может подключиться.</span><span class="sxs-lookup"><span data-stu-id="423e7-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="423e7-106">Вы можете использовать Netsh и сетевой монитор для получения и просмотра трассировок, чтобы определить причину сбоя подключения.</span><span class="sxs-lookup"><span data-stu-id="423e7-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="423e7-107">Во-первых, можно использовать Netsh для запуска трассировки.</span><span class="sxs-lookup"><span data-stu-id="423e7-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="423e7-108">Введите **команду netsh trace Start сценарий = WLAN TraceFile = вланвпп. ETL** запускает трассировку для всех поставщиков, включенных в сценарии WLAN, сохраняя результаты в файл с именем вланвпп. ETL.</span><span class="sxs-lookup"><span data-stu-id="423e7-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="423e7-109">После попытки подключения к беспроводной локальной сети введите **команду netsh trace остановить** завершается и сопоставляет файл трассировки.</span><span class="sxs-lookup"><span data-stu-id="423e7-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="423e7-110">Затем можно открыть файл вланвпп. ETL в сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="423e7-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="423e7-111">События группируются по ИДЕНТИФИКАТОРу действия на левой панели.</span><span class="sxs-lookup"><span data-stu-id="423e7-111">The events are grouped by activity ID in the left pane.</span></span>

![Устранение неполадок подключения к беспроводной локальной сети с помощью сетевого монитора (1)](images/1wlan.png)

<span data-ttu-id="423e7-113">ETL содержит много трассировок от других включенных поставщиков сети.</span><span class="sxs-lookup"><span data-stu-id="423e7-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="423e7-114">Можно применить фильтр, чтобы отобразить только те события, которые относятся к поставщику **\_ микрософтвиндовсвланаутоконфиг WLAN** .</span><span class="sxs-lookup"><span data-stu-id="423e7-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![Устранение неполадок подключения к беспроводной локальной сети с помощью сетевого монитора (2)](images/2wlan.png)

<span data-ttu-id="423e7-116">После применения фильтра можно проверить события в сводке кадров, чтобы узнать, какое событие будет иметь соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="423e7-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="423e7-117">После выбора события щелкните правой кнопкой мыши и наведите указатель на пункт найти беседы, а затем выберите Нетевент.</span><span class="sxs-lookup"><span data-stu-id="423e7-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![Устранение неполадок подключения к беспроводной локальной сети с помощью сетевого монитора (3)](images/3wlan.png)

<span data-ttu-id="423e7-119">Развернув элементы с ИДЕНТИФИКАТОРом действия на левой панели, вы сможете просмотреть все другие соответствующие поставщики для попытки подключения.</span><span class="sxs-lookup"><span data-stu-id="423e7-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="423e7-120">Чтобы просмотреть события от других поставщиков, необходимо удалить все фильтры, нажав кнопку **Удалить** на панели **фильтра отображения** .</span><span class="sxs-lookup"><span data-stu-id="423e7-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="423e7-121">Трассировки можно проанализировать, прокрутите сводку по кадрам, выбрав дополнительные события, необходимые для сбора дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="423e7-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="423e7-122">В этом случае область сведения о кадре содержит сведения об ошибке обмена ключами, скорее всего, из-за того, что пользователь вводит неверный ключ.</span><span class="sxs-lookup"><span data-stu-id="423e7-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




