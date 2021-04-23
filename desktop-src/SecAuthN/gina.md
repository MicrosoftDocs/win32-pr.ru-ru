---
description: БИБЛИОТЕКА GINA предназначена для предоставления настраиваемых процедур идентификации и аутентификации пользователей. GINA по умолчанию делает это путем делегирования отслеживания событий SAS в Winlogon, который получает и обрабатывает список безопасных сочетаний клавиш (Sasser) CTL + ALT + DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816048"
---
# <a name="gina"></a><span data-ttu-id="1ab44-104">GINA</span><span class="sxs-lookup"><span data-stu-id="1ab44-104">GINA</span></span>

<span data-ttu-id="1ab44-105">[*GINA*](/windows/desktop/SecGloss/g-gly) работает в [*контексте*](/windows/desktop/SecGloss/c-gly) процесса [*Winlogon*](/windows/desktop/SecGloss/w-gly) и, таким образом, DLL-библиотека GINA загружается на ранних этапах процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="1ab44-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="1ab44-106">Библиотека GINA DLL должна следовать правилам, чтобы обеспечить целостность системы, в частности в отношении взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1ab44-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="1ab44-107">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ab44-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="1ab44-108">Чаще всего GINA используется для связи с внешним устройством, таким как [*устройство чтения*](/windows/desktop/SecGloss/r-gly)смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="1ab44-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="1ab44-109">Важно установить параметр Start для драйвера устройства в значение System (Winnt. h: \_ Запуск системы службы \_ ), чтобы убедиться, что драйвер загружен на момент вызова GINA.</span><span class="sxs-lookup"><span data-stu-id="1ab44-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="1ab44-110">БИБЛИОТЕКА GINA предназначена для предоставления настраиваемых процедур идентификации и аутентификации пользователей.</span><span class="sxs-lookup"><span data-stu-id="1ab44-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="1ab44-111">GINA по умолчанию делает это путем делегирования отслеживания событий SAS в Winlogon, который получает и обрабатывает список [*безопасных сочетаний*](/windows/desktop/SecGloss/s-gly) клавиш (Sasser) CTL + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="1ab44-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="1ab44-112">Пользовательская GINA несет ответственность за настройку, чтобы получать события SAS (отличные от событий по умолчанию CTRL + ALT + DEL) и уведомлять об этом Winlogon при возникновении событий SAS.</span><span class="sxs-lookup"><span data-stu-id="1ab44-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="1ab44-113">Winlogon выполнит оценку своего состояния, чтобы определить, что необходимо для обработки SAS пользовательской модели GINA.</span><span class="sxs-lookup"><span data-stu-id="1ab44-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="1ab44-114">Эта обработка обычно включает вызовы функций обработки SAS модели GINA.</span><span class="sxs-lookup"><span data-stu-id="1ab44-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="1ab44-115">Сведения о конкретных функциях экспорта GINA см. в разделе [функции экспорта GINA](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1ab44-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="1ab44-116">Сведения об использовании структур GINA для передачи информации см. в разделе [модели GINA](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="1ab44-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="1ab44-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="1ab44-117">Topic</span></span>                                                                             | <span data-ttu-id="1ab44-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1ab44-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="1ab44-119">Загрузка и запуск библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="1ab44-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="1ab44-120">Значение раздела реестра, которое необходимо изменить для загрузки и запуска пользовательской библиотеки GINA.</span><span class="sxs-lookup"><span data-stu-id="1ab44-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="1ab44-121">Создание и тестирование библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="1ab44-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="1ab44-122">Тестирование библиотеки DLL GINA.</span><span class="sxs-lookup"><span data-stu-id="1ab44-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

