---
description: Поток может в любой момент вызвать Всаисблоккинг, чтобы определить, выполняется ли в данный момент блокирующий вызов.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Отмена блокирующих операций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701555"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="d743d-103">Отмена блокирующих операций</span><span class="sxs-lookup"><span data-stu-id="d743d-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="d743d-104">Поток может в любой момент вызвать [всаисблоккинг](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) , чтобы определить, выполняется ли в данный момент блокирующий вызов.</span><span class="sxs-lookup"><span data-stu-id="d743d-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="d743d-105">(Эта функция реализована в оболочках совместимости Windows Sockets 1,1 и, следовательно, не имеет аналога SPI.) Очевидно, что это возможно только в том случае, если псевдо-блокировка используется поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="d743d-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="d743d-106">При необходимости [**вспканцелблоккингкалл**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) может быть вызван в любое время для отмены любой текущей операции псевдо.</span><span class="sxs-lookup"><span data-stu-id="d743d-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
