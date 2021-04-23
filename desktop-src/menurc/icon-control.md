---
title: ЗНАЧОК элемента управления
description: Определяет элемент управления "значок". Этот элемент управления является значком, отображаемым в диалоговом окне.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Меню элементов управления "значок" и другие ресурсы
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487121"
---
# <a name="icon-control"></a><span data-ttu-id="b5e82-105">ЗНАЧОК элемента управления</span><span class="sxs-lookup"><span data-stu-id="b5e82-105">ICON control</span></span>

<span data-ttu-id="b5e82-106">Определяет элемент управления "значок".</span><span class="sxs-lookup"><span data-stu-id="b5e82-106">Defines an icon control.</span></span> <span data-ttu-id="b5e82-107">Этот элемент управления является значком, отображаемым в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="b5e82-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="b5e82-108">Оператор **Icon** , который можно использовать только в операторе [**диаложекс**](dialogex-resource.md) , определяет идентификатор значка ресурса, идентификатор элемента управления Icon, расположение и атрибуты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b5e82-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b5e82-109"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="b5e82-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="b5e82-110">Имя значка (а не имени файла), определенного в файле ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5e82-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="b5e82-111"><span id="width"></span><span id="WIDTH"></span>*Ширина*</span><span class="sxs-lookup"><span data-stu-id="b5e82-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="b5e82-112">Это значение игнорируется и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b5e82-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5e82-113"><span id="height"></span><span id="HEIGHT"></span>*равно*</span><span class="sxs-lookup"><span data-stu-id="b5e82-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="b5e82-114">Это значение игнорируется и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b5e82-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5e82-115"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="b5e82-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b5e82-116">Стиль элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b5e82-116">Control style.</span></span> <span data-ttu-id="b5e82-117">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b5e82-117">This parameter is optional.</span></span> <span data-ttu-id="b5e82-118">Единственным значением, которое можно указать, является стиль **\_ значка SS** .</span><span class="sxs-lookup"><span data-stu-id="b5e82-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="b5e82-119">Это стиль по умолчанию, определяющий, задан ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b5e82-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="b5e82-120">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b5e82-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b5e82-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="b5e82-121">Examples</span></span>

<span data-ttu-id="b5e82-122">В этом примере определяется элемент управления значком, идентификатором значка которого является 901, а имя — Микон:</span><span class="sxs-lookup"><span data-stu-id="b5e82-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="b5e82-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5e82-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e82-124">**ЗНАЧОК**</span><span class="sxs-lookup"><span data-stu-id="b5e82-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




