---
description: Сроки
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Сроки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684638"
---
# <a name="timeline"></a><span data-ttu-id="51150-103">Сроки</span><span class="sxs-lookup"><span data-stu-id="51150-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="51150-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="51150-104">\[Deprecated.</span></span> <span data-ttu-id="51150-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51150-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51150-106">Объект временной шкалы управляет всеми объектами в проекте редактирования видео.</span><span class="sxs-lookup"><span data-stu-id="51150-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="51150-107">Чтобы создать этот объект, вызовите **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="51150-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="51150-108">Идентификатор класса — CLSID \_ амтимелине.</span><span class="sxs-lookup"><span data-stu-id="51150-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="51150-109">Для чтения™ файлов Windows Media приложение должно предоставить сертификат программного обеспечения, который также называется ключом.</span><span class="sxs-lookup"><span data-stu-id="51150-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="51150-110">Зарегистрируйте приложение в качестве поставщика ключей через интерфейс **IObjectWithSite** временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="51150-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="51150-111">Дополнительные сведения см. [в разделе Разблокировка пакета SDK Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="51150-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="51150-112">Объект временной шкалы предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="51150-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="51150-113">**иамсетеррорлог**</span><span class="sxs-lookup"><span data-stu-id="51150-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="51150-114">**иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="51150-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="51150-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="51150-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="51150-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="51150-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="51150-117">См. также</span><span class="sxs-lookup"><span data-stu-id="51150-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51150-118">Модель временной шкалы</span><span class="sxs-lookup"><span data-stu-id="51150-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="51150-119">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="51150-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



