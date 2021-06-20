---
description: Узнайте о концепциях и функциях основных API-интерфейсов аудио в Windows Vista и об их использовании в программировании приложений.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Основные рекомендации по программированию аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405877"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="fa787-103">Основные рекомендации по программированию аудио</span><span class="sxs-lookup"><span data-stu-id="fa787-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="fa787-104">В этом разделе описываются основные понятия и функции основных API-интерфейсов аудио в Windows Vista, а также описывается, как использовать их в программировании приложений.</span><span class="sxs-lookup"><span data-stu-id="fa787-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="fa787-105">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="fa787-105">This section contains the following topics.</span></span>



| <span data-ttu-id="fa787-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="fa787-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="fa787-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fa787-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa787-108">Звуковые компоненты пользовательского режима</span><span class="sxs-lookup"><span data-stu-id="fa787-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="fa787-109">С помощью низкоуровневых интерфейсов в основных API-интерфейсах аудио клиент может получить доступ к системным компонентам, которые управляют и насмешивать звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="fa787-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="fa787-110">Звуковой режим защищенного пользователя (PUMA)</span><span class="sxs-lookup"><span data-stu-id="fa787-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="fa787-111">Описание обновлений для звука защищенного пользовательского режима (PUMA), подсистемы аудио пользовательского режима в защищенной среде (PE), которая предоставляет безопасную среду для обработки аудио и подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="fa787-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="fa787-112">Устройства конечных точек звука</span><span class="sxs-lookup"><span data-stu-id="fa787-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="fa787-113">Устройство конечной точки аудио является программной абстракцией, которая обеспечивает удобное взаимодействие с звуковыми устройствами, такими как микрофоны и динамики.</span><span class="sxs-lookup"><span data-stu-id="fa787-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="fa787-114">Сеансы аудио</span><span class="sxs-lookup"><span data-stu-id="fa787-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="fa787-115">Сеанс звука — это программная абстракция, которая позволяет клиенту управлять коллекцией связанных звуковых потоков как единое целое.</span><span class="sxs-lookup"><span data-stu-id="fa787-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="fa787-116">Регуляторы громкости</span><span class="sxs-lookup"><span data-stu-id="fa787-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="fa787-117">Система интегрирует свои параметры тома на основе политик с параметрами громкости пользователя в логическом и согласованном виде.</span><span class="sxs-lookup"><span data-stu-id="fa787-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="fa787-118">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="fa787-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="fa787-119">API сеанса Windows Audio (ВАСАПИ) предоставляет клиенту полный набор методов для создания и управления звуковыми потоками.</span><span class="sxs-lookup"><span data-stu-id="fa787-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="fa787-120">Топологии устройств</span><span class="sxs-lookup"><span data-stu-id="fa787-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="fa787-121">API Девицетопологи позволяет клиенту обнаруживать элементы управления звуком, которые находятся по различным путям к данным в звуковом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="fa787-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="fa787-122">Использование интерфейса Иксконтрол для доступа к свойствам аудио</span><span class="sxs-lookup"><span data-stu-id="fa787-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="fa787-123">Специализированному звуковому приложению может потребоваться использовать интерфейс Иксконтрол для доступа к свойствам звукового адаптера.</span><span class="sxs-lookup"><span data-stu-id="fa787-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="fa787-124">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="fa787-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="fa787-125">Основные возможности основных API-интерфейсов аудиоподсистемы в Windows Vista можно встроить в существующие приложения, использующие DirectSound, DirectShow и функции Windows мультимедиа **вавеауткскскс** и **вавеинкскскс** .</span><span class="sxs-lookup"><span data-stu-id="fa787-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="fa787-126">Пространственный звук</span><span class="sxs-lookup"><span data-stu-id="fa787-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="fa787-127">Руководство по использованию Windows Sonic, ориентированного на платформу решения для поддержки пространственного звука в Xbox и Windows, обеспечивающего как окружающие, так и повышенные звуковые подсказки (выше или ниже прослушивателя).</span><span class="sxs-lookup"><span data-stu-id="fa787-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fa787-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fa787-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa787-129">API-интерфейсы аудиоподсистемы Core</span><span class="sxs-lookup"><span data-stu-id="fa787-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



