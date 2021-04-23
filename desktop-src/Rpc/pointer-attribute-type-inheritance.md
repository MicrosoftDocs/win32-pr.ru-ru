---
title: Наследование типа Pointer-Attribute
description: В соответствии со спецификацией DCE каждый IDL-файл должен определять атрибуты для своих указателей.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413478"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="d7965-103">Наследование типа Pointer-Attribute</span><span class="sxs-lookup"><span data-stu-id="d7965-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="d7965-104">В соответствии со спецификацией DCE каждый IDL-файл должен определять атрибуты для своих указателей.</span><span class="sxs-lookup"><span data-stu-id="d7965-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="d7965-105">Если явный атрибут не назначен указателю, указатель использует значение, заданное \[ ключевым словом [указателя \_ по умолчанию](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="d7965-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="d7965-106">Некоторые реализации DCE не допускают указателей без атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d7965-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="d7965-107">Если указатель не имеет явного атрибута, IDL-файл должен иметь спецификацию **\[ \_ по умолчанию \] указателя** , чтобы можно было установить атрибут указателя.</span><span class="sxs-lookup"><span data-stu-id="d7965-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="d7965-108">В режиме по умолчанию (Microsoft-Extensions) можно указать атрибут указателя в IDL-файле, который импортирует определяющий IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="d7965-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="d7965-109">Указатели, определенные в одном IDL-файле, могут наследовать атрибуты, указанные в других IDL-файлах.</span><span class="sxs-lookup"><span data-stu-id="d7965-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="d7965-110">Кроме того, в режиме по умолчанию IDL-файлы могут включать указатели без атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d7965-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="d7965-111">Если ни базовый, ни импортированный IDL-файл не указал атрибут указателя или **\[ указатель \_ по умолчанию \]**, указатели без атрибутов будут интерпретированы как уникальные указатели.</span><span class="sxs-lookup"><span data-stu-id="d7965-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="d7965-112">Компилятор MIDL назначает атрибуты указателя указателям, используя следующие правила приоритета (1 — наивысший).</span><span class="sxs-lookup"><span data-stu-id="d7965-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="d7965-113">Приоритет</span><span class="sxs-lookup"><span data-stu-id="d7965-113">Priority</span></span> | <span data-ttu-id="d7965-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d7965-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7965-115">1</span><span class="sxs-lookup"><span data-stu-id="d7965-115">1</span></span>        | <span data-ttu-id="d7965-116">К указателю в определении или использовании сайта применяются явные атрибуты указателя.</span><span class="sxs-lookup"><span data-stu-id="d7965-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="d7965-117">2</span><span class="sxs-lookup"><span data-stu-id="d7965-117">2</span></span>        | <span data-ttu-id="d7965-118">По умолчанию используется атрибут **\[ указателя \_ по УМОЛЧАНИю \]** в IDL-файле, который определяет тип.</span><span class="sxs-lookup"><span data-stu-id="d7965-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="d7965-119">3</span><span class="sxs-lookup"><span data-stu-id="d7965-119">3</span></span>        | <span data-ttu-id="d7965-120">По умолчанию используется атрибут **\[ указателя \_ по УМОЛЧАНИю \]** в IDL-файле, который импортирует тип.</span><span class="sxs-lookup"><span data-stu-id="d7965-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="d7965-121">4</span><span class="sxs-lookup"><span data-stu-id="d7965-121">4</span></span>        | <span data-ttu-id="d7965-122">Значение по умолчанию — \[ [ptr](/windows/desktop/Midl/ptr) \] в режиме совместимости с DCE или \[ [уникальный](/windows/desktop/Midl/unique) \] в режиме расширения Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d7965-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 