---
title: аккнамеленгстулонг
description: аккнамеленгстулонг
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700694"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="cec8d-103">аккнамеленгстулонг</span><span class="sxs-lookup"><span data-stu-id="cec8d-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="cec8d-104">Текст</span><span class="sxs-lookup"><span data-stu-id="cec8d-104">Text</span></span>

<span data-ttu-id="cec8d-105">Имя элемента не должно возвращать строку длиннее {0} символа</span><span class="sxs-lookup"><span data-stu-id="cec8d-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="cec8d-106">Тип</span><span class="sxs-lookup"><span data-stu-id="cec8d-106">Type</span></span>

<span data-ttu-id="cec8d-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cec8d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="cec8d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cec8d-108">Description</span></span>

<span data-ttu-id="cec8d-109">Имя элемента содержит слишком много символов.</span><span class="sxs-lookup"><span data-stu-id="cec8d-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="cec8d-110">Например, метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, возвращает строку, превышающую ограничение в 32000 символов.</span><span class="sxs-lookup"><span data-stu-id="cec8d-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="cec8d-111">Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.</span><span class="sxs-lookup"><span data-stu-id="cec8d-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="cec8d-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="cec8d-112">Possible causes</span></span>

<span data-ttu-id="cec8d-113">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="cec8d-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cec8d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cec8d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec8d-115">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="cec8d-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="cec8d-116">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="cec8d-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




