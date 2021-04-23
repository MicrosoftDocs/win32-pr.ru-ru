---
title: аккнамеконтаинсинвалидстринг
description: аккнамеконтаинсинвалидстринг
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691368"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="00cda-103">аккнамеконтаинсинвалидстринг</span><span class="sxs-lookup"><span data-stu-id="00cda-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="00cda-104">Текст</span><span class="sxs-lookup"><span data-stu-id="00cda-104">Text</span></span>

<span data-ttu-id="00cda-105">Аккнаме не должно содержать строку {0}</span><span class="sxs-lookup"><span data-stu-id="00cda-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="00cda-106">Тип</span><span class="sxs-lookup"><span data-stu-id="00cda-106">Type</span></span>

<span data-ttu-id="00cda-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="00cda-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="00cda-108">Описание</span><span class="sxs-lookup"><span data-stu-id="00cda-108">Description</span></span>

<span data-ttu-id="00cda-109">Имя элемента содержит недопустимые символы (эти символы заменяются на Аккчеккер).</span><span class="sxs-lookup"><span data-stu-id="00cda-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="00cda-110">Например, метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, возвращает строку, содержащую символы табуляции, новой строки или амперсанда.</span><span class="sxs-lookup"><span data-stu-id="00cda-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="00cda-111">Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.</span><span class="sxs-lookup"><span data-stu-id="00cda-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="00cda-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="00cda-112">Possible causes</span></span>

<span data-ttu-id="00cda-113">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="00cda-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00cda-114">См. также</span><span class="sxs-lookup"><span data-stu-id="00cda-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00cda-115">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="00cda-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="00cda-116">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="00cda-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




