---
description: Общие сведения об использовании элементов управления без свойств субтитров для планшетных ПК.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Элементы управления без свойств субтитров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539437"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="7086a-103">Элементы управления без свойств субтитров</span><span class="sxs-lookup"><span data-stu-id="7086a-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="7086a-104">Если у элемента управления нет собственного свойства Caption, выполните следующие действия, чтобы убедиться, что вспомогательные средства могут обнаруживать элементы управления:</span><span class="sxs-lookup"><span data-stu-id="7086a-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="7086a-105">Создание статического текстового элемента управления с осмысленным и описательным именем.</span><span class="sxs-lookup"><span data-stu-id="7086a-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="7086a-106">Поместите статическую метку непосредственно перед элементом управления, на который указывает ссылка, в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="7086a-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="7086a-107">Убедитесь, что текст метки заканчивается двоеточием, например "Settings:".</span><span class="sxs-lookup"><span data-stu-id="7086a-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="7086a-108">Поместите текст метки непосредственно влево или выше элемента управления, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="7086a-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="7086a-109">Сделать статический текст невидимым, если он не подходит для визуального отображения.</span><span class="sxs-lookup"><span data-stu-id="7086a-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="7086a-110">Для этого нужно назначить соответствующий атрибут в скрипте ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7086a-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="7086a-111">Это может быть уместным, если имя или функция элемента управления визуально предоставляется средствами, отличными от статического элемента управления текстом, такого как рисунок или связанный переключатель.</span><span class="sxs-lookup"><span data-stu-id="7086a-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="7086a-112">Правильное использование статических элементов управления — единственный способ правильно реализовать подчеркнутые клавиши доступа для элементов управления, которые не имеют встроенных меток.</span><span class="sxs-lookup"><span data-stu-id="7086a-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="7086a-113">Дополнительные сведения об использовании элементов управления, не имеющих свойств заголовка, см. в разделе [Специальные возможности](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="7086a-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
