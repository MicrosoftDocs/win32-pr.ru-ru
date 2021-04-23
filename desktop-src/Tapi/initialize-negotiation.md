---
description: Тип \_ данных согласования инициализации — это специальное значение типа DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811213"
---
# <a name="initialize_negotiation"></a><span data-ttu-id="4e7e9-103">ИНИЦИАЛИЗАЦИя \_ согласования</span><span class="sxs-lookup"><span data-stu-id="4e7e9-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="4e7e9-104">Тип **данных \_ согласования инициализации** — это специальное значение типа **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="4e7e9-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="4e7e9-105">Его можно передать в качестве параметра *двдевицеид* в функции [**Тспи \_ линенеготиатетспиверсион**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) и [**тспи \_ фоненеготиатетспиверсион**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) .</span><span class="sxs-lookup"><span data-stu-id="4e7e9-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="4e7e9-106">Это означает, что TAPI может согласовать номер версии интерфейса ТСПИ независимо от конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="4e7e9-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
