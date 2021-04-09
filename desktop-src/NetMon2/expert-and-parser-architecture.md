---
description: На следующем рисунке показана связь между приложениями эксперта и анализатора и другими компонентами архитектуры сетевой монитор.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Архитектура эксперта и анализатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143819"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="16b25-103">Архитектура эксперта и анализатора</span><span class="sxs-lookup"><span data-stu-id="16b25-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="16b25-104">На следующем рисунке показана связь между приложениями [эксперта](experts.md) и [анализатора](parsers.md) и другими компонентами архитектуры сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="16b25-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![связь между экспертом и приложениями анализатора](images/nm-arch1.png)

<span data-ttu-id="16b25-106">Сетевой трафик собирается в виде отдельных кадров из драйвера NDIS.</span><span class="sxs-lookup"><span data-stu-id="16b25-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="16b25-107">Затем драйвер сетевой монитор (Nmnt.sys) направляет кадры в поставщик сетевых пакетов (НПП), который фиксирует данные и помещает их в один или несколько файлов записи.</span><span class="sxs-lookup"><span data-stu-id="16b25-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="16b25-108">НПП — это коллекция COM-интерфейсов, используемых для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="16b25-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="16b25-109">В этом случае для выполнения отложенной записи используется интерфейс [**иделайдк**](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="16b25-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="16b25-110">НПП используется для отложенных и в реальном времени записей.</span><span class="sxs-lookup"><span data-stu-id="16b25-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="16b25-111">Для записи в реальном времени используется интерфейс [**ИРТК**](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="16b25-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="16b25-112">Если кадры сети хранятся в файле записи, и файл доступен, эксперты и парсеры могут использовать пользовательский интерфейс сетевой монитор и функции сетевой монитор, предоставленные в Nmapi.dll для анализа данных.</span><span class="sxs-lookup"><span data-stu-id="16b25-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="16b25-113">Файлы записи недоступны до завершения записи.</span><span class="sxs-lookup"><span data-stu-id="16b25-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



