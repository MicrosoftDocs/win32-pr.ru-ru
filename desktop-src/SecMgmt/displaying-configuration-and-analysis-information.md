---
description: Расширение оснастки должно отображать текущие сведения о конфигурации и анализе для пользователей.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Отображение сведений о конфигурации и анализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683933"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="97d32-103">Отображение сведений о конфигурации и анализе</span><span class="sxs-lookup"><span data-stu-id="97d32-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="97d32-104">Расширение оснастки должно отображать текущие сведения о конфигурации и анализе для пользователей.</span><span class="sxs-lookup"><span data-stu-id="97d32-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="97d32-105">Чтобы отобразить сведения, узел расширения оснастки "вложение" должен расширить оснастку "Настройка безопасности" с помощью узла "службы".</span><span class="sxs-lookup"><span data-stu-id="97d32-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="97d32-106">Узел службы — это оснастка консоли управления (MMC), которая управляет службами, установленными в системе.</span><span class="sxs-lookup"><span data-stu-id="97d32-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="97d32-107">Ниже перечислены типы узлов, которые могут быть расширены.</span><span class="sxs-lookup"><span data-stu-id="97d32-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="97d32-108">Службы конфигурации NodeType = {24a7f717-1f0c-11D1-affb-00C04fB984F9}</span><span class="sxs-lookup"><span data-stu-id="97d32-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="97d32-109">Службы проверки NodeType = {678050c7-1ff8-11D1-affb-00C04fB984F9}</span><span class="sxs-lookup"><span data-stu-id="97d32-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="97d32-110">Когда узел службы развернут, MMC уведомляет все зарегистрированные расширения оснастки.</span><span class="sxs-lookup"><span data-stu-id="97d32-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="97d32-111">Каждая оснастка вложений должна быть вставлена в узел "службы" и выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="97d32-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="97d32-112">Вызовите **QueryInterface** , чтобы получить указатель на интерфейс [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) , предоставляемый оснасткой настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="97d32-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="97d32-113">Вызовите [**исцесвкаттачментдата:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) , чтобы сообщить оснасткам настройки безопасности о загрузке расширения оснастки и установить контекст для взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="97d32-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="97d32-114">Вызовите метод [**исцесвкаттачментдата:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) , чтобы получить сведения о конфигурации из базы данных.</span><span class="sxs-lookup"><span data-stu-id="97d32-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="97d32-115">Этот шаг можно выполнить либо при инициализации расширения оснастки, либо при открытии пользователем своего узла.</span><span class="sxs-lookup"><span data-stu-id="97d32-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="97d32-116">Дополнительные сведения см. [в разделе Добавление узла расширения оснастки «вложение](adding-an-attachment-snap-in-extension-node.md)».</span><span class="sxs-lookup"><span data-stu-id="97d32-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



