---
description: Перечисляет интерфейсы, предоставляемые подсистемой вложений.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Интерфейсы управления безопасностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684155"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="4b3c6-103">Интерфейсы управления безопасностью</span><span class="sxs-lookup"><span data-stu-id="4b3c6-103">Security Management Interfaces</span></span>

<span data-ttu-id="4b3c6-104">Этот раздел содержит справочные страницы для следующих групп интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="4b3c6-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="4b3c6-105">Интерфейсы подсистемы вложений</span><span class="sxs-lookup"><span data-stu-id="4b3c6-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="4b3c6-106">Интерфейсы подсистемы вложений</span><span class="sxs-lookup"><span data-stu-id="4b3c6-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="4b3c6-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="4b3c6-107">Interface</span></span>                                                            | <span data-ttu-id="4b3c6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4b3c6-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b3c6-109">**исцесвкаттачментдата**</span><span class="sxs-lookup"><span data-stu-id="4b3c6-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="4b3c6-110">Извлекает данные конфигурации и анализа для указанной службы безопасности из оснастки "Настройка безопасности". Оснастки "Настройка безопасности" предоставляют этот интерфейс, который вызывает расширения оснастки для запроса сведений о конфигурации или анализе.</span><span class="sxs-lookup"><span data-stu-id="4b3c6-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="4b3c6-111">**исцесвкаттачментперсистинфо**</span><span class="sxs-lookup"><span data-stu-id="4b3c6-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="4b3c6-112">Извлекает измененные сведения о конфигурации или анализе из оснастки вложений.</span><span class="sxs-lookup"><span data-stu-id="4b3c6-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="4b3c6-113">Оснастки настройки безопасности вызывают этот интерфейс для получения любых измененных сведений из расширения оснастки вложения.</span><span class="sxs-lookup"><span data-stu-id="4b3c6-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="4b3c6-114">Затем оснастка настройки безопасности сохраняет эти данные в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="4b3c6-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="4b3c6-115">Дополнительные сведения о COM-интерфейсах, которые должны быть реализованы с помощью расширений оснастки, см. в документации по [консоли управления Microsoft Management](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="4b3c6-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
