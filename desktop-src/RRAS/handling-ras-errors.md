---
title: Обработка ошибок RAS
description: При возникновении ошибки диспетчер подключений удаленного доступа вызывает обработчик уведомлений клиента.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS службы удаленного доступа, ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778404"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="2ae60-104">Обработка ошибок RAS</span><span class="sxs-lookup"><span data-stu-id="2ae60-104">Handling RAS Errors</span></span>

<span data-ttu-id="2ae60-105">При возникновении ошибки диспетчер подключений удаленного доступа вызывает обработчик уведомлений клиента.</span><span class="sxs-lookup"><span data-stu-id="2ae60-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="2ae60-106">Уведомление указывает состояние соединения при возникновении ошибки и код, определяющий ошибку.</span><span class="sxs-lookup"><span data-stu-id="2ae60-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="2ae60-107">В таких случаях обработчик уведомлений должен вызвать [**рашангуп**](/windows/desktop/api/Ras/nf-ras-rashangupa) для завершения подключения RAS.</span><span class="sxs-lookup"><span data-stu-id="2ae60-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="2ae60-108">Коды ошибок, которые определяют ошибки RAS, определяются в файле расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="2ae60-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="2ae60-109">Клиент RAS может использовать функцию [**расжетеррорстринг**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) для получения отображаемой строки, описывающей ошибку.</span><span class="sxs-lookup"><span data-stu-id="2ae60-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="2ae60-110">Описание этих ошибок см. в статье [коды ошибок маршрутизации и удаленного доступа](routing-and-remote-access-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae60-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




