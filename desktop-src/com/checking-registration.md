---
title: Проверка регистрации
description: Проверка регистрации
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986291"
---
# <a name="checking-registration"></a><span data-ttu-id="b670b-103">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="b670b-103">Checking Registration</span></span>

<span data-ttu-id="b670b-104">При каждой загрузке приложения необходимо проверить его регистрацию, чтобы определить следующее:</span><span class="sxs-lookup"><span data-stu-id="b670b-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="b670b-105">Содержатся ли в реестре идентификаторы CLSID.</span><span class="sxs-lookup"><span data-stu-id="b670b-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="b670b-106">Если они отсутствуют, приложение должно зарегистрироваться в качестве исходной установки.</span><span class="sxs-lookup"><span data-stu-id="b670b-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="b670b-107">Имеются ли в регистре CLSID приложения, но не имеющие в них сведений, относящихся к OLE 2.</span><span class="sxs-lookup"><span data-stu-id="b670b-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="b670b-108">В этом случае приложение должно зарегистрироваться в качестве исходной установки.</span><span class="sxs-lookup"><span data-stu-id="b670b-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="b670b-109">Указывает, указывают ли путь, содержащий записи сервера ([локалсервер](localserver.md) и [LocalServer32](localserver32.md), [Инпроксервер](inprocserver.md) и [InprocServer32](inprocserver32.md), и [дефаултикон](defaulticon.md)), на расположение, в котором приложение в настоящий момент установлено.</span><span class="sxs-lookup"><span data-stu-id="b670b-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="b670b-110">Если путь не имеет, перепишите записи пути, чтобы они указывали на текущее расположение.</span><span class="sxs-lookup"><span data-stu-id="b670b-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b670b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b670b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b670b-112">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="b670b-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




