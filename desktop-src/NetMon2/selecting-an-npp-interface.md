---
description: Поставщики сетевых пакетов (НППС) предоставляют интерфейсы Иделайдк, ИЕСП, ИРТК и Истатс.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Выбор интерфейса НПП
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898826"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="6be9c-103">Выбор интерфейса НПП</span><span class="sxs-lookup"><span data-stu-id="6be9c-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="6be9c-104">Поставщики сетевых пакетов (НППС) предоставляют интерфейсы [**иделайдк**](idelaydc.md), [**ИЕСП**](iesp.md), [**ИРТК**](irtc.md)и [**истатс**](istats.md) .</span><span class="sxs-lookup"><span data-stu-id="6be9c-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="6be9c-105">Каждый из этих интерфейсов предоставляет аналогичные методы для подключения НПП к сети, сбора сетевого трафика и сбора статистических данных о перехваченных данных.</span><span class="sxs-lookup"><span data-stu-id="6be9c-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="6be9c-106">Чтобы выбрать интерфейс для использования, обратитесь к следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6be9c-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="6be9c-107">При подключении НПП к сети с помощью одного из этих интерфейсов можно использовать только методы, предоставляемые этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="6be9c-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="6be9c-108">Например, если вы подключаетесь к сети с помощью интерфейса [**ИРТК**](irtc.md) , а затем пытаетесь начать запись с помощью [**иделайдк**](idelaydc.md), вызов для запуска записи завершится ошибкой и будет возвращен код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6be9c-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="6be9c-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="6be9c-109">Interface</span></span>                    | <span data-ttu-id="6be9c-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="6be9c-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6be9c-111">**иделайдк**</span><span class="sxs-lookup"><span data-stu-id="6be9c-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="6be9c-112">Используйте для записи сетевого трафика и сохранения его в файле записи.</span><span class="sxs-lookup"><span data-stu-id="6be9c-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="6be9c-113">Этот интерфейс используется сетевой монитор UI и другими приложениями НПП, для которых требуется хранить захваченные сведения о сети.</span><span class="sxs-lookup"><span data-stu-id="6be9c-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="6be9c-114">**иесп**</span><span class="sxs-lookup"><span data-stu-id="6be9c-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="6be9c-115">Используется для предоставления расширенной статистики в особом формате файла ESP.</span><span class="sxs-lookup"><span data-stu-id="6be9c-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="6be9c-116">Этот интерфейс используется приложениями НПП, для которых требуется расширенная статистика, предоставляемая форматом ESP.</span><span class="sxs-lookup"><span data-stu-id="6be9c-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="6be9c-117">**иртк**</span><span class="sxs-lookup"><span data-stu-id="6be9c-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="6be9c-118">Используется для сбора сетевого трафика в реальном времени и для активации событий при их возникновении.</span><span class="sxs-lookup"><span data-stu-id="6be9c-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="6be9c-119">Этот интерфейс используется приложениями НПП, для которых требуются записи времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="6be9c-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="6be9c-120">Обратите внимание, что этот интерфейс не предоставляет статистику, предоставляемую другими интерфейсами НПП, и не позволяет вставлять фреймы в захваченный сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="6be9c-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="6be9c-121">**истатс**</span><span class="sxs-lookup"><span data-stu-id="6be9c-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="6be9c-122">Используется для получения статистики записи, но не для захваченных кадров.</span><span class="sxs-lookup"><span data-stu-id="6be9c-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




