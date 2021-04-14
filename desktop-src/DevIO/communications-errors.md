---
description: Существуют и другие обстоятельства, когда операция чтения или записи может быть выполнена с меньшим числом символов, чем было запрошено, даже если время ожидания не истекло.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Ошибки связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496218"
---
# <a name="communications-errors"></a><span data-ttu-id="f85c4-103">Ошибки связи</span><span class="sxs-lookup"><span data-stu-id="f85c4-103">Communications Errors</span></span>

<span data-ttu-id="f85c4-104">Существуют и другие обстоятельства, когда операция чтения или записи может быть выполнена с меньшим числом символов, чем было запрошено, даже если время ожидания не истекло.</span><span class="sxs-lookup"><span data-stu-id="f85c4-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="f85c4-105">Ниже приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="f85c4-105">Following are some examples:</span></span>

-   <span data-ttu-id="f85c4-106">Некоторые драйверы поддерживают использование специальных символов, которые сразу же завершают операцию чтения с использованием только тех символов, которые были считаны до момента получения.</span><span class="sxs-lookup"><span data-stu-id="f85c4-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="f85c4-107">Функция [**пуржекомм**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) может быть вызвана для преждевременного завершения ожидающих операций чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="f85c4-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="f85c4-108">Эта функция также может удалять содержимое выходных или входных буферов либо и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="f85c4-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="f85c4-109">Если ошибка связи возникает во время операции чтения или записи, все операции ввода-вывода в ресурсе связи завершаются.</span><span class="sxs-lookup"><span data-stu-id="f85c4-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="f85c4-110">В качестве примера таких ошибок могут возблюдаться условия останова, ошибки четности или ошибки кадрирования.</span><span class="sxs-lookup"><span data-stu-id="f85c4-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="f85c4-111">При возникновении ошибки процесс должен вызвать функцию [**клеаркоммеррор**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) , чтобы сбросить флаг ошибки, прежде чем он сможет начать дополнительные операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f85c4-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="f85c4-112">**Клеаркоммеррор** сообщает о возникшей ошибке и текущем состоянии устройства.</span><span class="sxs-lookup"><span data-stu-id="f85c4-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



