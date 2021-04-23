---
description: Назначение по умолчанию можно изменить, просто вызвав Вспконнект еще раз, даже если сокет уже подключен. Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем Вспконнект.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Повторное подключение и отключение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898810"
---
# <a name="reconnecting-and-disconnecting"></a><span data-ttu-id="6a0af-104">Повторное подключение и отключение</span><span class="sxs-lookup"><span data-stu-id="6a0af-104">Reconnecting and Disconnecting</span></span>

<span data-ttu-id="6a0af-105">Назначение по умолчанию можно изменить, просто вызвав [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) еще раз, даже если сокет уже подключен.</span><span class="sxs-lookup"><span data-stu-id="6a0af-105">The default destination may be changed by simply calling [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) again, even if the socket is already connected.</span></span> <span data-ttu-id="6a0af-106">Все датаграммы, поставленные в очередь на получение, отбрасываются, если новый адрес отличается от адреса, указанного в предыдущем **вспконнект**.</span><span class="sxs-lookup"><span data-stu-id="6a0af-106">Any datagrams queued for receipt are discarded if the new address is different from the address specified in a previous **WSPConnect**.</span></span>

<span data-ttu-id="6a0af-107">Если адрес, указанный для сокета, равен нулю, сокет будет отключен — удаленный адрес по умолчанию будет неопределенным, поэтому вызовы [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) будут возвращать код ошибки всаенотконн, хотя [**вспсендто**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) и [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) по-прежнему могут использоваться.</span><span class="sxs-lookup"><span data-stu-id="6a0af-107">If the address supplied for the socket is all zeros, the socket will be disconnected — the default remote address will be indeterminate, so [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) calls will return the error code WSAENOTCONN, although [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) may still be used.</span></span>

 

 
