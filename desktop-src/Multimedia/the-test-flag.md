---
title: Флаг теста
description: Флаг теста
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Флаг MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332528"
---
# <a name="the-test-flag"></a><span data-ttu-id="6c85a-104">Флаг теста</span><span class="sxs-lookup"><span data-stu-id="6c85a-104">The Test Flag</span></span>

<span data-ttu-id="6c85a-105">Флаг Test ( \_ тест MCI) выполняет запрос устройства, чтобы определить, может ли он выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="6c85a-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="6c85a-106">Устройство возвращает ошибку, если не может выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="6c85a-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="6c85a-107">Он не возвращает ошибку, если может справиться с командой.</span><span class="sxs-lookup"><span data-stu-id="6c85a-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="6c85a-108">При указании этого флага MCI возвращает управление приложению, не выполняя команду.</span><span class="sxs-lookup"><span data-stu-id="6c85a-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="6c85a-109">Этот флаг поддерживается устройствами цифрового видео и ВИДЕОМАГНИТОФОНА для всех команд, кроме [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) и [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)).</span><span class="sxs-lookup"><span data-stu-id="6c85a-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




