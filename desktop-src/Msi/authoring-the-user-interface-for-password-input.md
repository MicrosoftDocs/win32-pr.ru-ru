---
description: Для каждого пароля, который должен быть задан пользователем, добавьте элемент управления Edit в диалоговое окно, в котором значение пароля сохраняется в свойстве.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Создание пользовательского интерфейса для ввода пароля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662932"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="e9257-103">Создание пользовательского интерфейса для ввода пароля</span><span class="sxs-lookup"><span data-stu-id="e9257-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="e9257-104">Для каждого пароля, который должен быть задан пользователем, добавьте элемент управления Edit в диалоговое окно, в котором значение пароля сохраняется в свойстве.</span><span class="sxs-lookup"><span data-stu-id="e9257-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="e9257-105">Этот [элемент управления](edit-control.md) "поле ввода" должен иметь [атрибут управления паролями](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="e9257-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="e9257-106">Это указывает, что указанное свойство является паролем и не позволяет установщику записывать свойство в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="e9257-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="e9257-107">[Атрибуты](control-attributes.md) элемента управления для элемента управления "поле ввода пароля": Мсидбконтролаттрибутесвисибле, Мсидбконтролаттрибутесенаблед и мсидбконтролаттрибутеспассвординпут (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="e9257-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="e9257-108">Значения X, Y, ширины, высоты и элемента управления \_ Далее зависят от макета элемента управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e9257-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="e9257-109">Таблица управления</span><span class="sxs-lookup"><span data-stu-id="e9257-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="e9257-110">Диалог\_</span><span class="sxs-lookup"><span data-stu-id="e9257-110">Dialog\_</span></span> | <span data-ttu-id="e9257-111">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="e9257-111">Control\_</span></span>            | <span data-ttu-id="e9257-112">Тип</span><span class="sxs-lookup"><span data-stu-id="e9257-112">Type</span></span> | <span data-ttu-id="e9257-113">X</span><span class="sxs-lookup"><span data-stu-id="e9257-113">X</span></span>   | <span data-ttu-id="e9257-114">Да</span><span class="sxs-lookup"><span data-stu-id="e9257-114">Y</span></span>   | <span data-ttu-id="e9257-115">Ширина</span><span class="sxs-lookup"><span data-stu-id="e9257-115">Width</span></span> | <span data-ttu-id="e9257-116">Высота:</span><span class="sxs-lookup"><span data-stu-id="e9257-116">Height</span></span> | <span data-ttu-id="e9257-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9257-117">Attributes</span></span> | <span data-ttu-id="e9257-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="e9257-118">Property</span></span>         | <span data-ttu-id="e9257-119">Текст</span><span class="sxs-lookup"><span data-stu-id="e9257-119">Text</span></span> | <span data-ttu-id="e9257-120">Управление \_ следующим</span><span class="sxs-lookup"><span data-stu-id="e9257-120">Control\_Next</span></span> | <span data-ttu-id="e9257-121">Справка</span><span class="sxs-lookup"><span data-stu-id="e9257-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="e9257-122">мидиалог</span><span class="sxs-lookup"><span data-stu-id="e9257-122">MyDialog</span></span> | <span data-ttu-id="e9257-123">тестусерпассвордедит</span><span class="sxs-lookup"><span data-stu-id="e9257-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="e9257-124">Изменить</span><span class="sxs-lookup"><span data-stu-id="e9257-124">Edit</span></span> | <span data-ttu-id="e9257-125">25</span><span class="sxs-lookup"><span data-stu-id="e9257-125">25</span></span>  | <span data-ttu-id="e9257-126">120</span><span class="sxs-lookup"><span data-stu-id="e9257-126">120</span></span> | <span data-ttu-id="e9257-127">300</span><span class="sxs-lookup"><span data-stu-id="e9257-127">300</span></span>   | <span data-ttu-id="e9257-128">20</span><span class="sxs-lookup"><span data-stu-id="e9257-128">20</span></span>     | <span data-ttu-id="e9257-129">2097155</span><span class="sxs-lookup"><span data-stu-id="e9257-129">2097155</span></span>    | <span data-ttu-id="e9257-130">тестусерпассворд</span><span class="sxs-lookup"><span data-stu-id="e9257-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="e9257-131">Отменить</span><span class="sxs-lookup"><span data-stu-id="e9257-131">Cancel</span></span>        |      |



 

<span data-ttu-id="e9257-132">Продолжайте [устанавливать защиту](securing-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="e9257-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



