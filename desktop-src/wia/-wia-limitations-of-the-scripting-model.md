---
description: Дополнительные сведения см. в статье ограничения модели сценариев.
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Ограничения модели скриптов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662403"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="77277-103">Ограничения модели скриптов</span><span class="sxs-lookup"><span data-stu-id="77277-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="77277-104">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="77277-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="77277-105">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="77277-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="77277-106">Модель скриптов для получения образа Windows (WIA) предоставляет подмножество функций WIA.</span><span class="sxs-lookup"><span data-stu-id="77277-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="77277-107">В следующей таблице приведены описания ограничений модели сценариев.</span><span class="sxs-lookup"><span data-stu-id="77277-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="77277-108">Функции WIA</span><span class="sxs-lookup"><span data-stu-id="77277-108">WIA Functionality</span></span>               | <span data-ttu-id="77277-109">Ограничение модели сценариев</span><span class="sxs-lookup"><span data-stu-id="77277-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77277-110">Подавление пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="77277-110">Suppressing the user interface</span></span>  | <span data-ttu-id="77277-111">Невозможно отключить пользовательский интерфейс для задания свойств устройства или перемещения.</span><span class="sxs-lookup"><span data-stu-id="77277-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="77277-112">установка свойств.</span><span class="sxs-lookup"><span data-stu-id="77277-112">Setting properties</span></span>              | <span data-ttu-id="77277-113">Невозможно задать (записать) все свойства устройства или элемента.</span><span class="sxs-lookup"><span data-stu-id="77277-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="77277-114">Регистрация для событий обратного вызова</span><span class="sxs-lookup"><span data-stu-id="77277-114">Registering for callback events</span></span> | <span data-ttu-id="77277-115">Может получить уведомление только для трех указанных событий: [**онтрансферкомплете**](-wia--iwiaevents-ontransfercomplete.md), [**ондевицеконнектед**](-wia--iwiaevents-ondeviceconnected.md)и [**ондевицедисконнектед**](-wia--iwiaevents-ondevicedisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="77277-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="77277-116">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="77277-116">Handling errors</span></span>                 | <span data-ttu-id="77277-117">Не удается выполнить обработку ошибок WIA.</span><span class="sxs-lookup"><span data-stu-id="77277-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
