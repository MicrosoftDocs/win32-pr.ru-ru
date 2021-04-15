---
title: уиаелементисорфанед
description: уиаелементисорфанед
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710093"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="7bf9f-103">уиаелементисорфанед</span><span class="sxs-lookup"><span data-stu-id="7bf9f-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="7bf9f-104">Текст</span><span class="sxs-lookup"><span data-stu-id="7bf9f-104">Text</span></span>

<span data-ttu-id="7bf9f-105">Элемент является потерянным элементом AutomationElement в дереве</span><span class="sxs-lookup"><span data-stu-id="7bf9f-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="7bf9f-106">Тип</span><span class="sxs-lookup"><span data-stu-id="7bf9f-106">Type</span></span>

<span data-ttu-id="7bf9f-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="7bf9f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7bf9f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7bf9f-108">Description</span></span>

<span data-ttu-id="7bf9f-109">Адрес интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) объекта, полученного для заданных координат, является ссылкой на потерянный элемент в дереве элементов.</span><span class="sxs-lookup"><span data-stu-id="7bf9f-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="7bf9f-110">Эта проблема возникает для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, поскольку элементы будут рассматриваться как невидимые и не будут объявлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="7bf9f-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7bf9f-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="7bf9f-111">Possible causes</span></span>

-   <span data-ttu-id="7bf9f-112">Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.</span><span class="sxs-lookup"><span data-stu-id="7bf9f-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="7bf9f-113">Неправильная или недопустимая реализация модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7bf9f-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bf9f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="7bf9f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf9f-115">**Иуиаутоматионелемент. Елементфромпоинт**</span><span class="sxs-lookup"><span data-stu-id="7bf9f-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




