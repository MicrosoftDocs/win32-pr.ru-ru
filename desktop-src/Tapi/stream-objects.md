---
description: Объекты потока являются абстракцией потока мультимедиа или потоков, связанных с сеансом вызова.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Объекты потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683709"
---
# <a name="stream-objects"></a><span data-ttu-id="e18dc-103">Объекты потока</span><span class="sxs-lookup"><span data-stu-id="e18dc-103">Stream Objects</span></span>

<span data-ttu-id="e18dc-104">Объекты потока являются абстракцией потока мультимедиа или потоков, связанных с сеансом вызова.</span><span class="sxs-lookup"><span data-stu-id="e18dc-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="e18dc-105">Интерфейсы и методы, предоставляемые для потоков и объектов подпотоков, позволяют приложению выполнять очень детализированные элементы управления, такие как приостановка потока, добавление новых типов мультимедиа в сеанс связи или корректировка громкости звука определенного участника конференции.</span><span class="sxs-lookup"><span data-stu-id="e18dc-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="e18dc-106">Два основных типа потока — это поток и подпоток.</span><span class="sxs-lookup"><span data-stu-id="e18dc-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="e18dc-107">Интерфейсы и методы стандартной реализации аналогичны для обоих типов, но для подпотоковой передачи, что обеспечивает более низкий уровень контроля.</span><span class="sxs-lookup"><span data-stu-id="e18dc-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="e18dc-108">Все поставщики служб мультимедиа (MSP) должны реализовывать базовые интерфейсы управления потоками, но поддержка для подпотоков является необязательной.</span><span class="sxs-lookup"><span data-stu-id="e18dc-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="e18dc-109">Кроме того, некоторые поставщики услуг реализуют [интерфейсы, зависящие от поставщика](provider-specific-interfaces.md) , для потоков.</span><span class="sxs-lookup"><span data-stu-id="e18dc-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="e18dc-110">Например, Ипконф MSP предоставляет элементы управления уровня участника.</span><span class="sxs-lookup"><span data-stu-id="e18dc-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="e18dc-111">Общие сведения см. в разделе [ИПКОНФ MSP interfaces](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="e18dc-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="e18dc-112">Другие интерфейсы, которые могут быть реализованы, см. в документации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e18dc-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="e18dc-113">MSP и TAPI создают объекты потока для вызова во время начальной настройки входящего или исходящего сеанса.</span><span class="sxs-lookup"><span data-stu-id="e18dc-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="e18dc-114">Приложение отвечает за определение соответствующих терминалов для этих потоков и выбор терминалов в потоках.</span><span class="sxs-lookup"><span data-stu-id="e18dc-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="e18dc-115">Обратите внимание, что в некоторых случаях MSP может потребовать, чтобы приложение остановило или приостанавливало потоки перед выполнением определенных операций сеанса вызова.</span><span class="sxs-lookup"><span data-stu-id="e18dc-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="e18dc-116">Интерфейсы потока описаны в [справочнике по интерфейсу поставщика службы мультимедиа (мспи)](media-service-provider-interface-mspi-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e18dc-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="e18dc-117">В примере с примером кода [терминала](select-a-terminal.md) показан пример перечисления потоков и выбора терминалов на них.</span><span class="sxs-lookup"><span data-stu-id="e18dc-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 



