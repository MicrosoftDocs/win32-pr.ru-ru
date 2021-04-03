---
title: Поддержка элементов обратного вызова
description: В этом разделе показано, как обеспечить поддержку элементов обратного вызова.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987997"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="8a48a-103">Поддержка элементов обратного вызова</span><span class="sxs-lookup"><span data-stu-id="8a48a-103">How to Support Callback Items</span></span>

<span data-ttu-id="8a48a-104">В этом разделе показано, как обеспечить поддержку элементов обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8a48a-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8a48a-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="8a48a-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8a48a-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="8a48a-106">Technologies</span></span>

-   [<span data-ttu-id="8a48a-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="8a48a-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8a48a-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8a48a-108">Prerequisites</span></span>

-   <span data-ttu-id="8a48a-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="8a48a-109">C/C++</span></span>
-   <span data-ttu-id="8a48a-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="8a48a-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8a48a-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8a48a-111">Instructions</span></span>


<span data-ttu-id="8a48a-112">Если приложение будет использовать элементы обратного вызова в элементе управления ComboBoxEx, необходимо подготовиться к обработке кода уведомления [ \_ жетдиспинфо кбен](cben-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8a48a-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="8a48a-113">Элемент управления ComboBoxEx отправляет это уведомление каждый раз, когда ему нужен владелец для предоставления конкретных сведений об элементе.</span><span class="sxs-lookup"><span data-stu-id="8a48a-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="8a48a-114">Дополнительные сведения об элементах обратного вызова см. в разделе [элементы обратного](comboboxex-controls.md)вызова.</span><span class="sxs-lookup"><span data-stu-id="8a48a-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="8a48a-115">Следующая определяемая приложением функция обрабатывает [кбен \_ жетдиспинфо](cben-getdispinfo.md) , предоставляя атрибуты для данного элемента.</span><span class="sxs-lookup"><span data-stu-id="8a48a-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="8a48a-116">Обратите внимание, что он устанавливает для элемента **маски** входящей [**КОМБОБОКСЕКСИТЕМ**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) структуры значение кбеиф \_ di \_ сетитем.</span><span class="sxs-lookup"><span data-stu-id="8a48a-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="8a48a-117">Если задать **маску** для этого значения, элемент управления будет хранить сведения об элементе, чтобы не запрашивать эти сведения еще раз.</span><span class="sxs-lookup"><span data-stu-id="8a48a-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="8a48a-118">Полный пример</span><span class="sxs-lookup"><span data-stu-id="8a48a-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="8a48a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8a48a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a48a-120">Сведения об элементах управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="8a48a-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="8a48a-121">Справочник по элементу управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="8a48a-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8a48a-122">Использование элементов управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="8a48a-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="8a48a-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="8a48a-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 