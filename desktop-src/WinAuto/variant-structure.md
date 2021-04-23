---
title: Структура варианта
description: Большинство функций Active Accessibility Microsoft, а также свойств и методов IAccessible принимают в качестве параметра структуру VARIANT. По сути, структура VARIANT — это контейнер для большого объединения, который содержит много типов данных.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134103"
---
# <a name="variant-structure"></a><span data-ttu-id="568d3-104">Структура варианта</span><span class="sxs-lookup"><span data-stu-id="568d3-104">VARIANT Structure</span></span>

<span data-ttu-id="568d3-105">Большинство функций Active Accessibility Microsoft, а также свойств и методов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) принимают в качестве параметра структуру [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="568d3-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="568d3-106">По сути, структура **Variant** — это контейнер для большого объединения, который содержит много типов данных.</span><span class="sxs-lookup"><span data-stu-id="568d3-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="568d3-107">Значение в первом члене структуры, **VT**, описывает, какое из членов Union является допустимым.</span><span class="sxs-lookup"><span data-stu-id="568d3-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="568d3-108">Хотя структура [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) поддерживает множество различных типов данных, Microsoft Active Accessibility использует только следующие типы.</span><span class="sxs-lookup"><span data-stu-id="568d3-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="568d3-109">Значение VT</span><span class="sxs-lookup"><span data-stu-id="568d3-109">vt Value</span></span>     | <span data-ttu-id="568d3-110">Имя соответствующего элемента значения</span><span class="sxs-lookup"><span data-stu-id="568d3-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="568d3-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="568d3-111">VT\_I4</span></span>       | <span data-ttu-id="568d3-112">**лвал**</span><span class="sxs-lookup"><span data-stu-id="568d3-112">**lVal**</span></span>                        |
| <span data-ttu-id="568d3-113">\_Диспетчер VT</span><span class="sxs-lookup"><span data-stu-id="568d3-113">VT\_DISPATCH</span></span> | <span data-ttu-id="568d3-114">**пдиспвал**</span><span class="sxs-lookup"><span data-stu-id="568d3-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="568d3-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="568d3-115">VT\_BSTR</span></span>     | <span data-ttu-id="568d3-116">**бстрвал**</span><span class="sxs-lookup"><span data-stu-id="568d3-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="568d3-117">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="568d3-117">VT\_EMPTY</span></span>    | <span data-ttu-id="568d3-118">нет</span><span class="sxs-lookup"><span data-stu-id="568d3-118">none</span></span>                            |



 

<span data-ttu-id="568d3-119">При получении сведений в структуре [**варианта**](/windows/win32/api/oaidl/ns-oaidl-variant) Проверьте элемент **VT** , чтобы узнать, какой элемент содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="568d3-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="568d3-120">Аналогично, при отправке данных с использованием структуры **Variant** всегда задавайте **VT** для отражения члена объединения, содержащего эти сведения.</span><span class="sxs-lookup"><span data-stu-id="568d3-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="568d3-121">Прежде чем использовать структуру, инициализируйте ее, вызвав функцию модели COM компонента [**вариантинит**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) .</span><span class="sxs-lookup"><span data-stu-id="568d3-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="568d3-122">После завершения работы со структурой очистите ее, прежде чем память, содержащая [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) , освобождается путем вызова [**вариантклеар**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span><span class="sxs-lookup"><span data-stu-id="568d3-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 