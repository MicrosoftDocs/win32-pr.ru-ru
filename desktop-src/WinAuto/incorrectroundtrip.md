---
title: инкорректраундтрип
description: инкорректраундтрип
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258786"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="3af18-103">инкорректраундтрип</span><span class="sxs-lookup"><span data-stu-id="3af18-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="3af18-104">Текст</span><span class="sxs-lookup"><span data-stu-id="3af18-104">Text</span></span>

<span data-ttu-id="3af18-105">Вызовите Аккнавигате ((щелкните отложить, чтобы напоминание снова в:), 1, НАВДИР \_ Далее), затем аккнавигате ((Open), 2, навдир \_ Previous), а затем нажмите кнопку отложить, чтобы напоминание снова в: (чилдид = 1), но возвращено нажмите кнопку отложить, чтобы снова выдавать напоминания в:</span><span class="sxs-lookup"><span data-stu-id="3af18-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="3af18-106">Тип</span><span class="sxs-lookup"><span data-stu-id="3af18-106">Type</span></span>

<span data-ttu-id="3af18-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="3af18-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="3af18-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3af18-108">Description</span></span>

<span data-ttu-id="3af18-109">использование [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) для прохода по дереву элементов целевого объекта проверки не возвращает тот же начальный элемент, когда направление обхода отменено.</span><span class="sxs-lookup"><span data-stu-id="3af18-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![Пример недопустимой реализации MSAA, которая привела к неправильной навигации по кругу](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="3af18-111">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="3af18-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="3af18-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="3af18-112">Possible causes</span></span>

<span data-ttu-id="3af18-113">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="3af18-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3af18-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3af18-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af18-115">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="3af18-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




