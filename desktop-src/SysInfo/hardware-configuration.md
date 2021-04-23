---
description: Функции конфигурации оборудования извлекают такие сведения, как процессор, профиль оборудования и сведения о клавиатуре.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Конфигурация оборудования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664353"
---
# <a name="hardware-configuration"></a><span data-ttu-id="d1b8e-103">Конфигурация оборудования</span><span class="sxs-lookup"><span data-stu-id="d1b8e-103">Hardware Configuration</span></span>

<span data-ttu-id="d1b8e-104">Функции конфигурации оборудования извлекают такие сведения, как процессор, профиль оборудования и сведения о клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-104">The hardware configuration functions retrieve information such as processor, hardware profile, and keyboard information.</span></span>

<span data-ttu-id="d1b8e-105">Функция [**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) извлекает сведения о процессоре и памяти, такие как размер страницы, идентификатор изготовителя оборудования, число и тип процессоров, диапазон адресов приложений и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-105">The [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function retrieves processor and memory information, such as the page size, original equipment manufacturer (OEM) identifier, number and type of processors, application address range, and so on.</span></span> <span data-ttu-id="d1b8e-106">Функция [**испроцессорфеатурепресент**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) извлекает сведения об операциях с плавающей запятой и наборах инструкций, поддерживаемых процессором.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-106">The [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) function retrieves information about the floating-point operations and instruction sets supported by the processor.</span></span>

<span data-ttu-id="d1b8e-107">Функция [**жеткурренсвпрофиле**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) извлекает сведения о профиле оборудования.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-107">The [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) function retrieves information about the hardware profile.</span></span> <span data-ttu-id="d1b8e-108">Профиль оборудования включает такие сведения, как состояние закрепления, глобальный уникальный идентификатор (GUID) и отображаемое имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-108">The hardware profile includes information such as the docking state, globally unique identifier (GUID), and display name for the profile.</span></span> <span data-ttu-id="d1b8e-109">Функция [**жеткэйбоардтипе**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) извлекает такую информацию, как тип клавиатуры и число функциональных клавиш на текущей клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="d1b8e-109">The [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) function retrieves such information as the type of keyboard and the number of function keys on the current keyboard.</span></span>

 

 
