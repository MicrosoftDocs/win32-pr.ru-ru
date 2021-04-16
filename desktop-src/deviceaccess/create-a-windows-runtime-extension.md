---
title: Создание среда выполнения Windows компонента для доступа к устройству
description: Можно создать компонент среда выполнения Windows, чтобы заключить в оболочку компонент, обращающийся к вашему драйверу. Затем вы можете написать приложение для Магазина Windows для устройства в C \ или JavaScript.
ms.assetid: 6CDFF247-DC78-4E90-B806-C25AB4F1129E
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bbf1d1e5766055197ed77366897a95ef4d1b79a5
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105719178"
---
# <a name="create-a-windows-runtime-component-for-device-access"></a><span data-ttu-id="de3d9-104">Создание среда выполнения Windows компонента для доступа к устройству</span><span class="sxs-lookup"><span data-stu-id="de3d9-104">Create a Windows Runtime component for device access</span></span>

<span data-ttu-id="de3d9-105">Можно создать компонент среда выполнения Windows, чтобы заключить в оболочку компонент, обращающийся к вашему драйверу.</span><span class="sxs-lookup"><span data-stu-id="de3d9-105">You can create a Windows Runtime component to wrap the component that accesses your driver.</span></span> <span data-ttu-id="de3d9-106">Затем можно написать приложение для Магазина Windows для устройства в C# или JavaScript.</span><span class="sxs-lookup"><span data-stu-id="de3d9-106">You can then write a Windows Store device app for your device in C# or JavaScript.</span></span>

## <a name="instructions"></a><span data-ttu-id="de3d9-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="de3d9-107">Instructions</span></span>

<span data-ttu-id="de3d9-108">См. [Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample). В этом примере реализуется среда выполнения Windows компонент для провидингсе функций специализированного устройства и используются функциональные возможности приложения для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="de3d9-108">See the [Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample).This sample implements a Windows Runtime component for providingthe functionality of a specialized device, and it uses the functionality in a Windows Store device app.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de3d9-109">См. также</span><span class="sxs-lookup"><span data-stu-id="de3d9-109">Related topics</span></span>

<span data-ttu-id="de3d9-110">[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="de3d9-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
