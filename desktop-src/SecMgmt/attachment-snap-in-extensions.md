---
description: Расширение оснастки вложений — это компонент вложения, который отображает пользовательский интерфейс, зависящий от службы.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Расширения оснастки вложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664843"
---
# <a name="attachment-snap-in-extensions"></a><span data-ttu-id="b14c7-103">Расширения оснастки вложений</span><span class="sxs-lookup"><span data-stu-id="b14c7-103">Attachment Snap-in Extensions</span></span>

<span data-ttu-id="b14c7-104">Расширение оснастки вложений — это компонент вложения, который отображает пользовательский интерфейс, зависящий от службы.</span><span class="sxs-lookup"><span data-stu-id="b14c7-104">An attachment snap-in extension is the component of an attachment that displays the service-specific user interface.</span></span> <span data-ttu-id="b14c7-105">Расширение оснастки размещается в оснастках настройки безопасности. Обмен данными между расширением вложений и узлом оснастки осуществляется стандартными механизмами MMC, описанными в документации по [консоли управления (Майкрософт](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="b14c7-105">The snap-in extension is hosted by the Security Configuration snap-ins. The communication between the attachment extension and its snap-in host is handled by the standard MMC mechanisms described in the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="b14c7-106">Помимо интерфейсов, которые должен поддерживать расширение оснастки, чтобы быть расширением оснастки MMC, расширение оснастки вложения также должно поддерживать COM-интерфейс [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="b14c7-106">In addition to the interfaces that the snap-in extension must support in order to be an MMC snap-in extension, an attachment snap-in extension must also support the COM interface, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="b14c7-107">Этот интерфейс реализует методы, которые указывают, существуют ли данные, относящиеся к службе, которые должны быть сохранены в базе данных безопасности, и, если это так, извлекают и сохраняют эти новые данные.</span><span class="sxs-lookup"><span data-stu-id="b14c7-107">This interface implements methods that indicate whether there is service-specific data that should be saved to the security database, and if so, retrieve and save this new data.</span></span> <span data-ttu-id="b14c7-108">Оснастки настройки безопасности вызывают методы этого интерфейса регулярно для обновления базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="b14c7-108">The Security Configuration snap-ins call methods of this interface regularly in order to update the security database.</span></span>

<span data-ttu-id="b14c7-109">Оснастки настройки безопасности реализуют интерфейс [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), который предоставляет методы для получения данных, относящихся к службе, из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="b14c7-109">The Security Configuration snap-ins implement an interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), that provides methods to retrieve service-specific data from the security database.</span></span> <span data-ttu-id="b14c7-110">Расширения оснастки вложений могут вызывать методы этого интерфейса для получения данных из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="b14c7-110">Attachment snap-in extensions can call methods of this interface to retrieve data from the security database.</span></span>

<span data-ttu-id="b14c7-111">Эта архитектура показана на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="b14c7-111">This architecture is illustrated in the following diagram.</span></span>

![расширения оснастки вложений](images/model2.png)

<span data-ttu-id="b14c7-113">При создании расширения оснастки вложения необходимо установить и зарегистрировать его с помощью оснасток настройки безопасности. Это можно сделать, добавив ключи в реестр, как описано в разделе [Регистрация расширения оснастки вложений](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="b14c7-113">When you create an attachment snap-in extension, you must install it and register it with the Security Configuration snap-ins. You do this by adding keys to the registry, as explained in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span> <span data-ttu-id="b14c7-114">При запуске оснастки настройки безопасности она проверяет реестр и загружает все зарегистрированные расширения оснастки.</span><span class="sxs-lookup"><span data-stu-id="b14c7-114">When a Security Configuration snap-in starts, it checks the registry and loads any registered snap-in extensions.</span></span> <span data-ttu-id="b14c7-115">Расширения отображаются в виде узлов в области безопасности для каждой службы в оснастке настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="b14c7-115">The extensions appear as nodes under the security area for each service in the Security Configuration snap-in.</span></span>

> [!Note]
> <span data-ttu-id="b14c7-116">Расширение оснастки вложений может расширять только узлы служб.</span><span class="sxs-lookup"><span data-stu-id="b14c7-116">An attachment snap-in extension can only extend Services nodes.</span></span> <span data-ttu-id="b14c7-117">Узел службы — это оснастка MMC, содержащая средства для администрирования служб, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="b14c7-117">The Services node is the MMC snap-in that contains tools to administer services installed on the system.</span></span> <span data-ttu-id="b14c7-118">Расширение оснастки вложения объявляет себя подчиненным для определенного типа узла служб, а затем для каждого вхождения этого типа узла консоль MMC автоматически добавляет соответствующие расширения оснастки.</span><span class="sxs-lookup"><span data-stu-id="b14c7-118">The attachment snap-in extension declares itself as being a subordinate to a specific Services node type, and then for each occurrence of that Services node type, the MMC console automatically adds the related snap-in extensions.</span></span>
> 
> <span data-ttu-id="b14c7-119">Каждое расширение оснастки вложений владеет одним узлом области области и связанной областью результатов в MMC.</span><span class="sxs-lookup"><span data-stu-id="b14c7-119">Each attachment snap-in extension owns one scope pane node and the related result pane in MMC.</span></span>

 

 

 
