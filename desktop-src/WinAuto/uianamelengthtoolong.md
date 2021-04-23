---
title: уианамеленгстулонг
description: уианамеленгстулонг
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- Идентификатор UIA_NamePropertyId AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411293"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="6c601-104">уианамеленгстулонг</span><span class="sxs-lookup"><span data-stu-id="6c601-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="6c601-105">Текст</span><span class="sxs-lookup"><span data-stu-id="6c601-105">Text</span></span>

<span data-ttu-id="6c601-106">Имя элемента не должно возвращать строку длиннее {0} символа</span><span class="sxs-lookup"><span data-stu-id="6c601-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="6c601-107">Тип</span><span class="sxs-lookup"><span data-stu-id="6c601-107">Type</span></span>

<span data-ttu-id="6c601-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="6c601-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6c601-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6c601-109">Description</span></span>

<span data-ttu-id="6c601-110">Имя элемента содержит слишком много символов.</span><span class="sxs-lookup"><span data-stu-id="6c601-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="6c601-111">Например, метод [**иуиаутоматионелемент:: куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) , используемый для получения имени UIA элемента, возвращает строку, превышающую ограничение.</span><span class="sxs-lookup"><span data-stu-id="6c601-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="6c601-112">Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.</span><span class="sxs-lookup"><span data-stu-id="6c601-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6c601-113">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="6c601-113">Possible causes</span></span>

<span data-ttu-id="6c601-114">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="6c601-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c601-115">См. также</span><span class="sxs-lookup"><span data-stu-id="6c601-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c601-116">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="6c601-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="6c601-117">**Иуиаутоматионелемент:: Куррентнаме**</span><span class="sxs-lookup"><span data-stu-id="6c601-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




