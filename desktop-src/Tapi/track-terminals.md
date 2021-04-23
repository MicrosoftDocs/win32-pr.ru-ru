---
description: Два типа терминалов определяют терминал записи и терминал воспроизведения, которые соответственно принадлежат и управляются терминалом записи файлов и терминалом воспроизведения файлов.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Мониторинг терминалов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684000"
---
# <a name="track-terminals"></a><span data-ttu-id="27663-103">Мониторинг терминалов</span><span class="sxs-lookup"><span data-stu-id="27663-103">Track Terminals</span></span>

<span data-ttu-id="27663-104">Определяются два типа терминалов: терминал записи и терминал воспроизведения, которые, соответственно, принадлежат и управляются терминалом записи файлов и терминалом воспроизведения файлов.</span><span class="sxs-lookup"><span data-stu-id="27663-104">Two types of track terminals are defined: Recording Track Terminal and Playback Track Terminal, which, respectively, belong to and are managed by File Recording Terminal and File Playback Terminal.</span></span>

<span data-ttu-id="27663-105">Все терминалы мониторинга предоставляют интерфейсы [**итфилетракк**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) и [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="27663-105">All track terminals expose the [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) and [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interfaces.</span></span> <span data-ttu-id="27663-106">Интерфейс **иттерминал** позволяет выбрать терминалы для мониторинга на потоки или вызовы.</span><span class="sxs-lookup"><span data-stu-id="27663-106">The **ITTerminal** interface allows the selection of track terminals onto streams or calls.</span></span>

> [!Note]  
> <span data-ttu-id="27663-107">Мониторинг терминалов также предоставляет частный интерфейс [**итмедиаконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), который использует MSP.</span><span class="sxs-lookup"><span data-stu-id="27663-107">Track terminals also expose a private interface, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), which the MSP uses.</span></span> <span data-ttu-id="27663-108">Приложения не должны пытаться получить доступ к этому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="27663-108">Applications should not attempt to access this interface.</span></span>

 

 

 
