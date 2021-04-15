---
title: ОПЕРАТОРЕ EXSTYLE, инструкция
description: Определяет расширенные стили окна для диалогового окна. В определении ресурса инструкция ОПЕРАТОРЕ EXSTYLE помещается с необязательными инструкциями перед началом тела определения ресурса.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Меню инструкций ОПЕРАТОРЕ EXSTYLE и другие ресурсы
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487620"
---
# <a name="exstyle-statement"></a><span data-ttu-id="2ad6c-105">ОПЕРАТОРЕ EXSTYLE, инструкция</span><span class="sxs-lookup"><span data-stu-id="2ad6c-105">EXSTYLE statement</span></span>

<span data-ttu-id="2ad6c-106">Определяет расширенные стили окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="2ad6c-107">В определении ресурса инструкция **операторе EXSTYLE** помещается с необязательными инструкциями перед началом тела определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="2ad6c-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Расширенный стиль*</span><span class="sxs-lookup"><span data-stu-id="2ad6c-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="2ad6c-109">Расширенный стиль окна для диалогового окна или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="2ad6c-110">Список расширенных стилей окон см. в разделе [**Расширенные стили окон**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="2ad6c-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ad6c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ad6c-111">Remarks</span></span>

<span data-ttu-id="2ad6c-112">Для элементов управления расширенные стили задаются после параметра *Style* в операторе Control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="2ad6c-113">Дополнительные сведения см. в описании инструкции Resource-Definition для отдельного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ad6c-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ad6c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad6c-115">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-116">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-117">**Откроется**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-118">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-119">**ПОДСКАЗКИ**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-121">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="2ad6c-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="2ad6c-122">Определяемый пользователем ресурс</span><span class="sxs-lookup"><span data-stu-id="2ad6c-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 