---
title: Выбор дочерних объектов
description: Клиенты вызывают метод IAccessible Аккселект для изменения выделения или фокуса клавиатуры между дочерними элементами объекта. Константы СЕЛФЛАГ, указанные с помощью вызова, определяют выполняемую операцию.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328912"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="c02f5-104">Выбор дочерних объектов</span><span class="sxs-lookup"><span data-stu-id="c02f5-104">Selecting Child Objects</span></span>

<span data-ttu-id="c02f5-105">Клиенты вызывают метод [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) для изменения выделения или фокуса клавиатуры между дочерними элементами объекта.</span><span class="sxs-lookup"><span data-stu-id="c02f5-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="c02f5-106">[Константы селфлаг](selflag.md) , указанные с помощью вызова, определяют выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="c02f5-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="c02f5-107">Если метод [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) вызывается с флагом [**селфлаг \_ такефокус**](selflag.md) для дочернего объекта, имеющего **HWND**, флаг вступает в силу только в том случае, если родительский объект объекта имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="c02f5-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="c02f5-108">Выполнение сложных операций выбора</span><span class="sxs-lookup"><span data-stu-id="c02f5-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="c02f5-109">Ниже описано, какие значения СЕЛФЛАГ необходимо указать при вызове метода [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) для выполнения сложных операций выбора.</span><span class="sxs-lookup"><span data-stu-id="c02f5-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="c02f5-110">**Имитация щелчка**</span><span class="sxs-lookup"><span data-stu-id="c02f5-110">**To simulate a click**</span></span>

-   <span data-ttu-id="c02f5-111">[**Селфлаг \_ такефокус**](selflag.md) \| [ **селфлаг \_ такеселектион**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="c02f5-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="c02f5-112">**Выбор целевого элемента путем имитации щелчка CTRL + щелчок**</span><span class="sxs-lookup"><span data-stu-id="c02f5-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="c02f5-113">[**Селфлаг \_ такефокус**](selflag.md) \| [ **селфлаг \_ аддселектион**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="c02f5-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="c02f5-114">**Отмена выбора целевого элемента путем имитации нажатия клавиш CTRL + щелчок**</span><span class="sxs-lookup"><span data-stu-id="c02f5-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="c02f5-115">[**Селфлаг \_ такефокус**](selflag.md) \| [ **селфлаг \_ ремовеселектион**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="c02f5-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="c02f5-116">**Имитация НАЖАТия SHIFT + щелчок**</span><span class="sxs-lookup"><span data-stu-id="c02f5-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="c02f5-117">[**Селфлаг \_ такефокус**](selflag.md) \| [ **селфлаг \_ екстендселектион**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="c02f5-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="c02f5-118">**Выбор диапазона объектов и помещение фокуса на последний объект**</span><span class="sxs-lookup"><span data-stu-id="c02f5-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="c02f5-119">Укажите [**селфлаг \_ такефокус**](selflag.md) на начальном объекте, чтобы задать привязку выбора.</span><span class="sxs-lookup"><span data-stu-id="c02f5-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="c02f5-120">Вызовите метод [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) еще раз и укажите [**селфлаг \_ екстендселектион**](selflag.md) \| [**селфлаг \_ такефокус**](selflag.md) на последнем объекте.</span><span class="sxs-lookup"><span data-stu-id="c02f5-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="c02f5-121">**Чтобы отменить выбор всех объектов**</span><span class="sxs-lookup"><span data-stu-id="c02f5-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="c02f5-122">Укажите [**селфлаг \_ такеселектион**](selflag.md) для любого объекта.</span><span class="sxs-lookup"><span data-stu-id="c02f5-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="c02f5-123">Этот флаг отменяет выбор всех выбранных объектов, кроме одного выбранного.</span><span class="sxs-lookup"><span data-stu-id="c02f5-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="c02f5-124">Вызовите метод [**IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) еще раз и укажите [**селфлаг \_ ремовеселектион**](selflag.md) для оставшегося объекта.</span><span class="sxs-lookup"><span data-stu-id="c02f5-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




