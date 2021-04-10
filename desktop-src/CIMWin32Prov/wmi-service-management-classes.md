---
description: Классы управления службами WMI используются для управления самой службой WMI, а не компьютерной системой или корпоративной сетью. Управление WMI включает в себя настройку службы WMI и управление операциями WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Классы управления службами WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141031"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="9731d-104">Классы управления службами WMI</span><span class="sxs-lookup"><span data-stu-id="9731d-104">WMI Service Management Classes</span></span>

<span data-ttu-id="9731d-105">Классы управления службами WMI используются для управления самой службой WMI, а не компьютерной системой или корпоративной сетью.</span><span class="sxs-lookup"><span data-stu-id="9731d-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="9731d-106">Управление WMI включает в себя настройку службы WMI и управление операциями WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="9731d-107">Категория управления службами WMI включает следующие подкатегории классов.</span><span class="sxs-lookup"><span data-stu-id="9731d-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="9731d-108">Классы конфигурации WMI</span><span class="sxs-lookup"><span data-stu-id="9731d-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="9731d-109">Классы управления WMI</span><span class="sxs-lookup"><span data-stu-id="9731d-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="9731d-110">Классы конфигурации WMI</span><span class="sxs-lookup"><span data-stu-id="9731d-110">WMI Configuration Classes</span></span>

<span data-ttu-id="9731d-111">Класс конфигурации WMI наследует методы, которые настраивают службу WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="9731d-112">Ниже приведена таблица классов конфигурации WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="9731d-113">Класс</span><span class="sxs-lookup"><span data-stu-id="9731d-113">Class</span></span>                                                             | <span data-ttu-id="9731d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9731d-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="9731d-115">**\_Месодпараметеркласс Win32**</span><span class="sxs-lookup"><span data-stu-id="9731d-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="9731d-116">Абстрактный базовый класс, который реализует параметры метода, производные от этого класса.</span><span class="sxs-lookup"><span data-stu-id="9731d-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="9731d-117">Классы управления WMI</span><span class="sxs-lookup"><span data-stu-id="9731d-117">WMI Management Classes</span></span>

<span data-ttu-id="9731d-118">Классы управления WMI представляют операционные параметры для службы WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="9731d-119">Ниже приведена таблица классов управления WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="9731d-120">Класс</span><span class="sxs-lookup"><span data-stu-id="9731d-120">Class</span></span>                                                       | <span data-ttu-id="9731d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9731d-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9731d-122">**\_Вмисеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9731d-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="9731d-123">Содержит рабочие параметры для службы WMI.</span><span class="sxs-lookup"><span data-stu-id="9731d-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="9731d-124">**\_Вмиелементсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9731d-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="9731d-125">Связь между службой, работающей в системе Windows, и параметрами WMI, которые она может использовать.</span><span class="sxs-lookup"><span data-stu-id="9731d-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9731d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9731d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9731d-127">Классы Win32</span><span class="sxs-lookup"><span data-stu-id="9731d-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
