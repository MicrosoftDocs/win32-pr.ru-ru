---
title: Архитектура микшера
description: Архитектура микшера
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- мультимедийные аудио, архитектура микшера
- аудио, архитектура микшера
- аудио миксерс, архитектура
- звуковые миксерсы, звуковые линии
- звуковые линии
- аудио миксерс, элементы управления
- мультимедиа аудио, элементы управления микшера
- аудио, элементы управления микшера
- миксерс, звуковые строки
- миксерс, архитектура
- миксерс, элементы управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329784"
---
# <a name="mixer-architecture"></a><span data-ttu-id="363c9-114">Архитектура микшера</span><span class="sxs-lookup"><span data-stu-id="363c9-114">Mixer Architecture</span></span>

<span data-ttu-id="363c9-115">Основной элемент архитектуры микшера — это *звуковая линия*.</span><span class="sxs-lookup"><span data-stu-id="363c9-115">The basic element of the mixer architecture is an *audio line*.</span></span> <span data-ttu-id="363c9-116">Звуковая строка состоит из одного или нескольких каналов данных, исходящих из одного источника или системного ресурса.</span><span class="sxs-lookup"><span data-stu-id="363c9-116">An audio line consists of one or more channels of data originating from a single source or a system resource.</span></span> <span data-ttu-id="363c9-117">Например, в стереосистеме есть два канала данных, но они рассматриваются как одна звуковая строка, так как она происходит из одного источника.</span><span class="sxs-lookup"><span data-stu-id="363c9-117">For example, a stereo audio line has two data channels, but it is considered a single audio line because it originates from a single source.</span></span>

<span data-ttu-id="363c9-118">Архитектура микшера предоставляет службы маршрутизации для управления звуковыми линиями на компьютере.</span><span class="sxs-lookup"><span data-stu-id="363c9-118">The mixer architecture provides routing services to manage audio lines on a computer.</span></span> <span data-ttu-id="363c9-119">Службы маршрутизации можно использовать, если установлены соответствующие аппаратные устройства и драйверы программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="363c9-119">You can use the routing services if you have adequate hardware devices and software drivers installed.</span></span> <span data-ttu-id="363c9-120">Архитектура микшера позволяет нескольким строкам аудио источника сопоставляться с одной конечной строкой назначения.</span><span class="sxs-lookup"><span data-stu-id="363c9-120">The mixer architecture allows several audio source lines to map to a single destination audio line.</span></span>

<span data-ttu-id="363c9-121">С каждой звуковой линией могут быть связаны элементы управления микшера.</span><span class="sxs-lookup"><span data-stu-id="363c9-121">Each audio line can have mixer controls associated with it.</span></span> <span data-ttu-id="363c9-122">Элемент управления микшера может выполнять любое количество функций (например, управляющий том) в зависимости от характеристик соответствующей звуковой линии.</span><span class="sxs-lookup"><span data-stu-id="363c9-122">A mixer control can perform any number of functions (such as control volume), depending on the characteristics of the associated audio line.</span></span>

 

 




