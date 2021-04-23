---
description: Обработчик трассировки программного обеспечения Windows (WPP) обеспечивает эффективный механизм регистрации событий, происходящих во время выполнения приложения или драйвера. Интерфейс WPP использует API ETW.
ms.assetid: 3a6f441a-ae36-4cce-aa83-78a4e53c9b1a
title: Создание событий WPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f0d4deb580a3f81f3c6c87f6ca5ca4518f735e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984548"
---
# <a name="writing-wpp-events"></a><span data-ttu-id="2c1c2-104">Создание событий WPP</span><span class="sxs-lookup"><span data-stu-id="2c1c2-104">Writing WPP Events</span></span>

<span data-ttu-id="2c1c2-105">Обработчик трассировки программного обеспечения Windows (WPP) обеспечивает эффективный механизм регистрации событий, происходящих во время выполнения приложения или драйвера.</span><span class="sxs-lookup"><span data-stu-id="2c1c2-105">The Windows software trace processor (WPP) provides an efficient mechanism to log events that occur during the execution of an application or driver.</span></span> <span data-ttu-id="2c1c2-106">Интерфейс WPP использует API ETW.</span><span class="sxs-lookup"><span data-stu-id="2c1c2-106">WPP uses the ETW API.</span></span>

<span data-ttu-id="2c1c2-107">Дополнительные сведения об использовании конвейера WPP для регистрации событий см. в разделе [часто задаваемые вопросы](/windows-hardware/drivers/devtest/software-tracing-faq) о [трассировке программного обеспечения](/windows-hardware/drivers/devtest/wpp-software-tracing) и программном обеспечении в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="2c1c2-107">For details on using WPP to log events, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Software Tracing FAQ](/windows-hardware/drivers/devtest/software-tracing-faq) in the Microsoft Windows Driver Development Kit (DDK).</span></span>

 

 
