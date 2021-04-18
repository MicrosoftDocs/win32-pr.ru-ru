---
description: Расширение оснастки «вложение» предоставляет интерфейс, который пользователи могут использовать для изменения параметров конфигурации, зависящих от службы.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Создание расширения оснастки «вложение»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683934"
---
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="5e820-103">Создание расширения оснастки «вложение»</span><span class="sxs-lookup"><span data-stu-id="5e820-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="5e820-104">Расширение оснастки «вложение» предоставляет интерфейс, который пользователи могут использовать для изменения параметров конфигурации, зависящих от службы.</span><span class="sxs-lookup"><span data-stu-id="5e820-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="5e820-105">Расширение оснастки "вложение" должно соответствовать требованиям MMC, чтобы быть допустимым расширением оснастки.</span><span class="sxs-lookup"><span data-stu-id="5e820-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="5e820-106">Дополнительные сведения об этих требованиях см. в документации по [консоли управления Microsoft Management](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="5e820-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="5e820-107">В дополнение к интерфейсам, необходимым для MMC, расширение оснастки вложения должно реализовывать COM-интерфейс [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="5e820-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="5e820-108">Оснастки настройки безопасности вызывают методы этого интерфейса, чтобы определить, изменились ли данные конфигурации, и, если да, обновить базу данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="5e820-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="5e820-109">Оснастка "вложение" должна сохранять любые изменения конфигурации до тех пор, пока оснастки настройки безопасности не извлекают эти данные.</span><span class="sxs-lookup"><span data-stu-id="5e820-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="5e820-110">Расширение оснастки вложений должно обеспечивать следующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="5e820-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="5e820-111">Отображение сведений о конфигурации и анализе</span><span class="sxs-lookup"><span data-stu-id="5e820-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="5e820-112">Изменение сведений о конфигурации в пользовательском интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5e820-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="5e820-113">Изменение сведений о конфигурации в базе данных безопасности</span><span class="sxs-lookup"><span data-stu-id="5e820-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="5e820-114">Чтобы помочь вашему расширению оснастки при выполнении этих задач, оснастки настройки безопасности реализуют COM-интерфейс [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), предоставляющий методы, которые может вызывать расширение оснастки для инициализации и запроса сведений из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="5e820-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="5e820-115">После создания расширения оснастки вложения необходимо зарегистрировать его с помощью оснасток настройки безопасности, как описано в разделе [Регистрация расширения оснастки вложений](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="5e820-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 
