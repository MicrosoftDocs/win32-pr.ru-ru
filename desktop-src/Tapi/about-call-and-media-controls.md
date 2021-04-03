---
description: Элементы управления вызовами и мультимедиа TAPI 3 — это универсальный набор COM-объектов, интерфейсов и методов для выполнения вызовов между двумя или более компьютерами.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: О вызовах и элементах управления мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914183"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="05976-103">О вызовах и элементах управления мультимедиа</span><span class="sxs-lookup"><span data-stu-id="05976-103">About Call And Media Controls</span></span>

<span data-ttu-id="05976-104">Элементы управления вызовами и мультимедиа TAPI 3 — это универсальный набор COM-объектов, интерфейсов и методов для выполнения вызовов между двумя или более компьютерами.</span><span class="sxs-lookup"><span data-stu-id="05976-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="05976-105">В контексте TAPI 3 *вызов* относится не только к передаче голоса через коммутируемую телефонную сеть с открытым коммутируемым доступом (PSTN), но и к любому среднему и транспортному механизму, для которого существуют поставщики услуг. Например, Конференция мультимедиа многоадресной рассылки, запущенной в корпоративной интрасети.</span><span class="sxs-lookup"><span data-stu-id="05976-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="05976-106">Пять основных объектов в вызове TAPI 3 и архитектура управления мультимедиа — это [TAPI](tapi-object.md), [адрес](address-object.md), [терминал](terminal-object.md), [вызов](call-object.md)и [каллхуб](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="05976-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="05976-107">Кроме того, для [интерфейсов, зависящих от поставщика](provider-specific-interfaces.md), предпринята инициализация.</span><span class="sxs-lookup"><span data-stu-id="05976-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="05976-108">На следующей схеме показано, как взаимодействуют эти объекты.</span><span class="sxs-lookup"><span data-stu-id="05976-108">The following diagram illustrates how these objects interact.</span></span>

![взаимодействие между вызовами TAPI 3,0 и объектами управления мультимедиа](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="05976-110">Компоненты</span><span class="sxs-lookup"><span data-stu-id="05976-110">Features</span></span>

-   <span data-ttu-id="05976-111">Абстрактные функции вызова и мультимедиа, позволяющие различным и похоже несовместимым протоколам связи предоставлять общий интерфейс приложениям.</span><span class="sxs-lookup"><span data-stu-id="05976-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="05976-112">На основе модели COM, так что приложения могут быть написаны практически на любом языке.</span><span class="sxs-lookup"><span data-stu-id="05976-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="05976-113">Если вам требуются дополнительные сведения об COM, ознакомьтесь с пакетом SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="05976-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="05976-114">Управление вызовами предоставляется поставщиками услуг телефонии (специалистами), которые реализуют механизмы, связанные с транспортом.</span><span class="sxs-lookup"><span data-stu-id="05976-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="05976-115">Управление носителями, предоставляемое поставщиками служб мультимедиа (MSP).</span><span class="sxs-lookup"><span data-stu-id="05976-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="05976-116">Current MSP использовать DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05976-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="05976-117">DirectShow — это модульная система подключаемых компонентов, называемых фильтрами, которая упорядочена в конфигурации, называемой графом фильтра.</span><span class="sxs-lookup"><span data-stu-id="05976-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="05976-118">Диспетчер графов фильтров видит соединение этих фильтров и управляет потоком данных потока.</span><span class="sxs-lookup"><span data-stu-id="05976-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="05976-119">Если вам требуются дополнительные сведения о DirectShow, ознакомьтесь с пакетом SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="05976-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



