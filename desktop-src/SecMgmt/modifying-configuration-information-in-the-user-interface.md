---
description: Расширение оснастки "вложение" должно позволять пользователю изменять сведения о конфигурации службы.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Изменение сведений о конфигурации в пользовательском интерфейсе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664217"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a><span data-ttu-id="b0ae3-103">Изменение сведений о конфигурации в пользовательском интерфейсе</span><span class="sxs-lookup"><span data-stu-id="b0ae3-103">Modifying Configuration Information in the User Interface</span></span>

<span data-ttu-id="b0ae3-104">Расширение оснастки "вложение" должно позволять пользователю изменять сведения о конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="b0ae3-104">An attachment snap-in extension must allow the user to modify configuration information about the service.</span></span> <span data-ttu-id="b0ae3-105">Измененные данные должны храниться в расширении оснастки «вложение» до тех пор, пока оснастка настройки безопасности не вызовет методы интерфейса [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) для получения информации.</span><span class="sxs-lookup"><span data-stu-id="b0ae3-105">The modified information should be stored by the attachment snap-in extension until the Security Configuration snap-in calls methods of the [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interface to retrieve the information.</span></span>

<span data-ttu-id="b0ae3-106">Чтобы избежать утечек памяти, освободите память, выделенную подключаемым модулем, вызвав [**исцесвкаттачментперсистинфо:: фрибуффер**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).</span><span class="sxs-lookup"><span data-stu-id="b0ae3-106">To avoid memory leaks, free memory allocated by the snap-in extension by calling [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).</span></span>

 

 



