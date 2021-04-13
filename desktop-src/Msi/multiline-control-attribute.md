---
description: Если этот бит установлен в элементе управления "поле ввода", установщик создает многострочный элемент управления "поле ввода" с вертикальной полосой прокрутки.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Атрибут элемента управления MultiLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263956"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="6e597-103">Атрибут элемента управления MultiLine</span><span class="sxs-lookup"><span data-stu-id="6e597-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="6e597-104">Если этот бит установлен в [элементе управления](edit-control.md)"поле ввода", установщик создает многострочный элемент управления "поле ввода" с вертикальной полосой прокрутки.</span><span class="sxs-lookup"><span data-stu-id="6e597-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="6e597-105">Если этот бит не задан, он задает отображение обычного элемента управления "Правка".</span><span class="sxs-lookup"><span data-stu-id="6e597-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6e597-106">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="6e597-106">Valid Controls</span></span>

<span data-ttu-id="6e597-107">[Изменить элемент управления](edit-control.md).</span><span class="sxs-lookup"><span data-stu-id="6e597-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="6e597-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="6e597-108">Decimal</span></span> | <span data-ttu-id="6e597-109">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="6e597-109">Hexadecimal</span></span> | <span data-ttu-id="6e597-110">Константа</span><span class="sxs-lookup"><span data-stu-id="6e597-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="6e597-111">65536</span><span class="sxs-lookup"><span data-stu-id="6e597-111">65536</span></span>   | <span data-ttu-id="6e597-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6e597-112">0x00010000</span></span>  | <span data-ttu-id="6e597-113">**мсидбконтролаттрибутесмултилине**</span><span class="sxs-lookup"><span data-stu-id="6e597-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e597-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e597-114">Remarks</span></span>

<span data-ttu-id="6e597-115">Чтобы задать этот атрибут для элемента управления, включите многострочный бит в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6e597-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6e597-116">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6e597-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



