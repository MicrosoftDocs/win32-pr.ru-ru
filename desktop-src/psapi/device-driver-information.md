---
title: Сведения о драйвере устройства
description: Драйверы устройств и модули аналогичны тем, что они основаны на файлах PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067598"
---
# <a name="device-driver-information"></a><span data-ttu-id="85ef2-103">Сведения о драйвере устройства</span><span class="sxs-lookup"><span data-stu-id="85ef2-103">Device Driver Information</span></span>

<span data-ttu-id="85ef2-104">Драйверы устройств и модули аналогичны тем, что они основаны на файлах PE.</span><span class="sxs-lookup"><span data-stu-id="85ef2-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="85ef2-105">Однако, хотя каждый процесс имеет собственный частный список загруженных модулей, драйверы устройств имеют глобальные модули для системы.</span><span class="sxs-lookup"><span data-stu-id="85ef2-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="85ef2-106">Таким образом, PSAPI имеет определенные функции для получения списка драйверов устройств и их имен.</span><span class="sxs-lookup"><span data-stu-id="85ef2-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="85ef2-107">Вы можете получить адрес загрузки для каждого драйвера устройства, вызвав функцию [**енумдевицедриверс**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) .</span><span class="sxs-lookup"><span data-stu-id="85ef2-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="85ef2-108">Эта функция заполняет массив значений **лпвоид** , используя адреса загрузки всех драйверов устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="85ef2-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="85ef2-109">Функция [**жетдевицедривербасенаме**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) принимает адрес загрузки драйвера в качестве входных данных и заполняет буфер базовым именем драйвера (например, Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="85ef2-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="85ef2-110">Связанная функция, [**жетдевицедриверфиленаме**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), принимает те же параметры и возвращает путь к драйверу устройства (например, C: \\ Windows \\ system32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="85ef2-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




