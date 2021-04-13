---
title: Завершение сеанса проверки подлинности
description: После завершения сеанса аутентификации служба проверки подлинности вызывает функцию Расеапенд, чтобы разрешить протоколу проверки подлинности освободить рабочий буфер.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412852"
---
# <a name="completion-of-the-authentication-session"></a><span data-ttu-id="c8462-103">Завершение сеанса проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c8462-103">Completion of the Authentication Session</span></span>

<span data-ttu-id="c8462-104">После завершения сеанса аутентификации служба проверки подлинности вызывает функцию [**расеапенд**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) , чтобы разрешить протоколу проверки подлинности освободить рабочий буфер.</span><span class="sxs-lookup"><span data-stu-id="c8462-104">After the authentication session is completed, the authentication service calls the [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) function to allow the authentication protocol to deallocate its work buffer.</span></span> <span data-ttu-id="c8462-105">Это действие принимается независимо от того, была ли проверка подлинности успешной.</span><span class="sxs-lookup"><span data-stu-id="c8462-105">This action is taken regardless of whether authentication was successful.</span></span> <span data-ttu-id="c8462-106">Вызов функции **расеапенд** гарантирует, что никакие дальнейшие вызовы к протоколу проверки подлинности с помощью этого конкретного пользователя или контекста не будут выполнены без предварительного вызова [**расеапбегин**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8462-106">Calling the **RasEapEnd** function guarantees that no further calls are made to the authentication protocol using that particular user or context without first calling [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).</span></span>

 

 