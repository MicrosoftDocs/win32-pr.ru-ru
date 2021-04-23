---
title: Проверка подлинности безопасности сервера RAS
description: Когда сервер удаленного доступа Windows NT или Windows 2000 получает вызов, он вызывает функцию Рассекуритидиалогбегин зарегистрированной DLL-библиотеки безопасности RAS, если таковая имеется.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067882"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="0d60c-103">Проверка подлинности безопасности сервера RAS</span><span class="sxs-lookup"><span data-stu-id="0d60c-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="0d60c-104">Когда сервер удаленного доступа Windows NT или Windows 2000 получает вызов, он вызывает функцию [**рассекуритидиалогбегин**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) зарегистрированной DLL-библиотеки безопасности RAS, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="0d60c-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="0d60c-105">Этот вызов уведомляет библиотеку DLL безопасности, чтобы начать проверку подлинности удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d60c-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="0d60c-106">Сервер RAS вызывает **рассекуритидиалогбегин** перед выполнением проверки подлинности PPP или RAS.</span><span class="sxs-lookup"><span data-stu-id="0d60c-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="0d60c-107">Вызов [**рассекуритидиалогбегин**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) передает следующие сведения в библиотеку DLL безопасности:</span><span class="sxs-lookup"><span data-stu-id="0d60c-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="0d60c-108">Маркер порта для обнаружения соединения.</span><span class="sxs-lookup"><span data-stu-id="0d60c-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="0d60c-109">Указатели на буферы, используемые при взаимодействии с удаленным пользователем.</span><span class="sxs-lookup"><span data-stu-id="0d60c-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="0d60c-110">Указатель на функцию [**рассекуритидиалогкомплете**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) для вызова после завершения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0d60c-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="0d60c-111">Маркер порта и указатель буфера допустимы до тех пор, пока библиотека DLL безопасности не вызовет [**рассекуритидиалогкомплете**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) для завершения транзакции проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0d60c-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="0d60c-112">[**Рассекуритидиалогкомплете**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) уведомляет сервер RAS о результатах проверки подлинности удаленного пользователя в библиотеке DLL безопасности.</span><span class="sxs-lookup"><span data-stu-id="0d60c-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="0d60c-113">Если библиотека DLL безопасности сообщает об успешном выполнении, сервер удаленного доступа переходит в систему с проверкой подлинности PPP и RAS удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d60c-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="0d60c-114">Если DLL-библиотека безопасности сообщает, что удаленный пользователь не прошел проверку подлинности или произошла ошибка, сервер RAS зависает и записывает в журнал событий ошибку или неудачную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="0d60c-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




