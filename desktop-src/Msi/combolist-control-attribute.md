---
description: Если для поля со списком задан бит управления Комболист, поле редактирования заменяется статическим текстовым полем. Это предотвращает ввод пользователем нового значения и требует, чтобы пользователь выбрал только одно из предопределенных значений.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Атрибут элемента управления Комболист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663981"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="df042-104">Атрибут элемента управления Комболист</span><span class="sxs-lookup"><span data-stu-id="df042-104">ComboList Control Attribute</span></span>

<span data-ttu-id="df042-105">Если для поля со списком задан бит управления Комболист, поле редактирования заменяется статическим текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="df042-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="df042-106">Это предотвращает ввод пользователем нового значения и требует, чтобы пользователь выбрал только одно из предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="df042-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="df042-107">Если этот бит не задан, поле со списком содержит поле редактирования.</span><span class="sxs-lookup"><span data-stu-id="df042-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="df042-108">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="df042-108">Valid Controls</span></span>

[<span data-ttu-id="df042-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="df042-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="df042-110">Значение</span><span class="sxs-lookup"><span data-stu-id="df042-110">Value</span></span>



| <span data-ttu-id="df042-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="df042-111">Decimal</span></span> | <span data-ttu-id="df042-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="df042-112">Hexadecimal</span></span> | <span data-ttu-id="df042-113">Описание</span><span class="sxs-lookup"><span data-stu-id="df042-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="df042-114">131072</span><span class="sxs-lookup"><span data-stu-id="df042-114">131072</span></span>  | <span data-ttu-id="df042-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="df042-115">0x00020000</span></span>  | <span data-ttu-id="df042-116">мсидбконтролаттрибутескомболист</span><span class="sxs-lookup"><span data-stu-id="df042-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="df042-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df042-117">Remarks</span></span>

<span data-ttu-id="df042-118">Чтобы задать этот атрибут для элемента управления, включите бит Комболист в столбец Attributes записи элемента управления в [таблице Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="df042-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="df042-119">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="df042-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



