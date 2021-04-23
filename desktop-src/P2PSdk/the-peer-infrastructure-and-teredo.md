---
description: Пользователь может проверить состояние интерфейса Teredo из командной строки, введя команду netsh interface Teredo показывать состояние и проверив выходные данные.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: Одноранговая инфраструктура и Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545519"
---
# <a name="the-peer-infrastructure-and-teredo"></a><span data-ttu-id="e8083-103">Одноранговая инфраструктура и Teredo</span><span class="sxs-lookup"><span data-stu-id="e8083-103">The Peer Infrastructure and Teredo</span></span>

<span data-ttu-id="e8083-104">Пользователь может проверить состояние интерфейса [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) из командной строки, введя команду **netsh interface Teredo показывать состояние** и проверив выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e8083-104">A user can check the status of the [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) interface from the command prompt by typing **netsh interface teredo show state** and examining the output.</span></span> <span data-ttu-id="e8083-105">Если состояние имеет значение "отключено", Teredo не активен, что запрещает пользователю подключаться к другим пользователям через адреса Teredo.</span><span class="sxs-lookup"><span data-stu-id="e8083-105">If the state is "offline", Teredo is not active, which prevents the user from connecting to other users via their Teredo addresses.</span></span> <span data-ttu-id="e8083-106">Возможно, Teredo находится в автономном режиме, так как брандмауэр отключен или не поддерживает [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="e8083-106">It is possible Teredo may be offline because your firewall is disabled or does not support [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span></span>

 

 
