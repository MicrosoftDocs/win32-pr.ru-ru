---
title: уианамешаулднотконтаинконтролтипе
description: уианамешаулднотконтаинконтролтипе
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888075"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="2f18f-103">уианамешаулднотконтаинконтролтипе</span><span class="sxs-lookup"><span data-stu-id="2f18f-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="2f18f-104">Текст</span><span class="sxs-lookup"><span data-stu-id="2f18f-104">Text</span></span>

<span data-ttu-id="2f18f-105">Имя элемента ( {0} ) не должно содержать текст ControlType ( {1} )</span><span class="sxs-lookup"><span data-stu-id="2f18f-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="2f18f-106">Тип</span><span class="sxs-lookup"><span data-stu-id="2f18f-106">Type</span></span>

<span data-ttu-id="2f18f-107">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="2f18f-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="2f18f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2f18f-108">Description</span></span>

<span data-ttu-id="2f18f-109">Имя элемента включает свой тип элемента управления UIA.</span><span class="sxs-lookup"><span data-stu-id="2f18f-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="2f18f-110">Например, это предупреждение может возникать, если для свойства "имя UIA" элемента с типом элемента управления "Кнопка" задано значение "Моя кнопка".</span><span class="sxs-lookup"><span data-stu-id="2f18f-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="2f18f-111">Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку тип элемента управления будет прочитан дважды или не может быть неясным или интуитивно понятным для пользователей.</span><span class="sxs-lookup"><span data-stu-id="2f18f-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2f18f-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="2f18f-112">Possible causes</span></span>

-   <span data-ttu-id="2f18f-113">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="2f18f-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="2f18f-114">Элемент или его родитель имеет имя по умолчанию, которое не было изменено на понятное имя.</span><span class="sxs-lookup"><span data-stu-id="2f18f-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="2f18f-115">Например, button1.</span><span class="sxs-lookup"><span data-stu-id="2f18f-115">For example, button1.</span></span>
-   <span data-ttu-id="2f18f-116">Разработчик не знает, что читатели экрана считывают имена и типы элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2f18f-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f18f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2f18f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f18f-118">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f18f-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="2f18f-119">**Иуиаутоматионелемент:: Куррентнаме**</span><span class="sxs-lookup"><span data-stu-id="2f18f-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




