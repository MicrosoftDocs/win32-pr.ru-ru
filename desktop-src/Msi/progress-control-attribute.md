---
description: Этот атрибут измеряет, насколько далеко заполняется индикатор индикатора хода выполнения.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Атрибут элемента управления progress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651150"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="6bc5f-103">Атрибут элемента управления progress</span><span class="sxs-lookup"><span data-stu-id="6bc5f-103">Progress Control Attribute</span></span>

<span data-ttu-id="6bc5f-104">Этот атрибут измеряет, насколько далеко заполняется индикатор индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="6bc5f-105">Запись содержит два целых числа и строку.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-105">The record contains two integers and a string.</span></span> <span data-ttu-id="6bc5f-106">Первое число — это ход выполнения, второе число — диапазон (максимально возможное число для хода выполнения).</span><span class="sxs-lookup"><span data-stu-id="6bc5f-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="6bc5f-107">При значении целые числа могут быть указаны в виде целочисленных полей или строк, содержащих целые числа.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="6bc5f-108">Если второе число отсутствует, предполагается, что используется значение по умолчанию (1024).</span><span class="sxs-lookup"><span data-stu-id="6bc5f-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="6bc5f-109">Если ход выполнения больше, чем диапазон, он изменяется на диапазон.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="6bc5f-110">Третье поле — это строка, имя действия, для которого отображается ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="6bc5f-111">Дополнительные сведения см. в статьях [Создание элемента управления ProgressBar](authoring-a-progressbar-control.md)и [Добавление настраиваемых действий в ProgressBar](adding-custom-actions-to-the-progressbar.md).</span><span class="sxs-lookup"><span data-stu-id="6bc5f-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6bc5f-112">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="6bc5f-112">Valid Controls</span></span>

[<span data-ttu-id="6bc5f-113">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="6bc5f-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="6bc5f-114">Связанные битовые флаги</span><span class="sxs-lookup"><span data-stu-id="6bc5f-114">Associated Bit Flags</span></span>

<span data-ttu-id="6bc5f-115">Этот атрибут не использует битовые флаги.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc5f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bc5f-116">Remarks</span></span>

<span data-ttu-id="6bc5f-117">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6bc5f-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



