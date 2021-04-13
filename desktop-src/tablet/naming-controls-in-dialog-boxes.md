---
description: При использовании диалоговых окон Microsoft Windows необходимо пометить все элементы управления, чтобы упростить работу с речью. В следующем диалоговом окне Выполнение отображается метка статического текстового элемента управления для раскрывающегося списка. Статический текст заканчивается двоеточием.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Именование элементов управления в диалоговых окнах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568680"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="9685e-105">Именование элементов управления в диалоговых окнах</span><span class="sxs-lookup"><span data-stu-id="9685e-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="9685e-106">При использовании диалоговых окон Microsoft Windows необходимо пометить все элементы управления, чтобы упростить работу с речью.</span><span class="sxs-lookup"><span data-stu-id="9685e-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="9685e-107">В следующем диалоговом окне **выполнение** отображается метка статического текстового элемента управления для раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="9685e-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="9685e-108">Статический текст заканчивается двоеточием.</span><span class="sxs-lookup"><span data-stu-id="9685e-108">Static text ends with a colon.</span></span>

![снимок экрана с диалоговым окном "выполнить"](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="9685e-110">Существуют два типа элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9685e-110">There are two types of controls:</span></span>

-   <span data-ttu-id="9685e-111">Элементы управления, имеющие заголовки в качестве свойства этого элемента управления, такие как кнопки команд и флажки.</span><span class="sxs-lookup"><span data-stu-id="9685e-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="9685e-112">Вспомогательные средства не имеют возможности идентифицировать эти элементы управления, пока заголовок правильно определен.</span><span class="sxs-lookup"><span data-stu-id="9685e-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="9685e-113">Элементы управления, у которых нет собственных заголовков, таких как элементы управления редактирования, списки и представления списков, должны помечаться с помощью отдельных статических элементов управления "текст".</span><span class="sxs-lookup"><span data-stu-id="9685e-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="9685e-114">Дополнительные сведения об элементах управления, которые не имеют собственных заголовков, см. в разделе [элементы управления без свойств субтитров](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9685e-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="9685e-115">Несколько методов можно использовать для преодоления ситуаций, в которых элементы управления не имеют собственных заголовков, но они эффективны только для окон, отображаемых стандартным диспетчером диалоговых окон (SDM).</span><span class="sxs-lookup"><span data-stu-id="9685e-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="9685e-116">Все остальные окна должны предоставлять имена и отношения между элементами управления путем явной поддержки Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9685e-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="9685e-117">Дополнительные сведения о Active Accessibility см. в разделе [Специальные возможности](/windows/desktop/accessibility) библиотеки MSDN.</span><span class="sxs-lookup"><span data-stu-id="9685e-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
