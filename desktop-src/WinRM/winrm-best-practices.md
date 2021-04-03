---
title: Рекомендации по WinRM
description: В этом разделе объясняются некоторые рекомендации по использованию различных функций API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987562"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="c074d-103">Рекомендации по WinRM</span><span class="sxs-lookup"><span data-stu-id="c074d-103">WinRM Best Practices</span></span>

<span data-ttu-id="c074d-104">В этом разделе объясняются некоторые рекомендации по использованию различных функций API WinRM.</span><span class="sxs-lookup"><span data-stu-id="c074d-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="c074d-105">Квоты</span><span class="sxs-lookup"><span data-stu-id="c074d-105">Quotas</span></span>

<span data-ttu-id="c074d-106">При достижении квоты служба WinRM возвращает клиенту сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c074d-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="c074d-107">В результате клиентская логика должна явным образом повторить операцию на основе возвращенной ошибки.</span><span class="sxs-lookup"><span data-stu-id="c074d-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="c074d-108">Подписки на события</span><span class="sxs-lookup"><span data-stu-id="c074d-108">Event subscriptions</span></span>

<span data-ttu-id="c074d-109">При использовании подписок, инициированных сборщиком, ограничьте число удаленных компьютеров до 500 и изолируйте службу [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) (вексвк) в отдельном хост-процессе.</span><span class="sxs-lookup"><span data-stu-id="c074d-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="c074d-110">Ошибка подключения будет содержать поток до истечения времени ожидания. Большое количество одновременных ошибок подключения может привести к нехватке пула потоков и отрисовывать сервер без ответа.</span><span class="sxs-lookup"><span data-stu-id="c074d-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 