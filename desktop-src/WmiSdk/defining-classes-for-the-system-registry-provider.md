---
description: Приложение управления, использующее поставщик системного реестра, может определять классы со свойствами, представляющими данные реестра для определенных ключей, а затем сохранять классы в репозитории WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Определение классов для поставщика системного реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999062"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="f1cf1-103">Определение классов для поставщика системного реестра</span><span class="sxs-lookup"><span data-stu-id="f1cf1-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="f1cf1-104">Приложение управления, использующее поставщик системного реестра, может определять классы со свойствами, представляющими данные реестра для определенных ключей, а затем сохранять классы в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="f1cf1-105">Большинство процессов определения класса для системного реестра идентичны определению любого другого класса.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="f1cf1-106">Однако поставщик системного реестра требует использования конкретных типов данных и квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="f1cf1-107">В следующей процедуре описывается определение класса для поставщика системного реестра.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="f1cf1-108">**Определение класса для поставщика системного реестра**</span><span class="sxs-lookup"><span data-stu-id="f1cf1-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="f1cf1-109">Создайте класс так же, как любой другой класс.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="f1cf1-110">Дополнительные сведения см. [в разделе Создание класса](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="f1cf1-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="f1cf1-111">Сопоставьте соответствующие типы данных реестра с соответствующими типами WMI.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="f1cf1-112">Поставщик системного реестра сопоставляет типы данных реестра с конкретными типами данных WMI.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="f1cf1-113">Дополнительные сведения см. в разделе [сопоставление типа данных реестра с типом данных WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="f1cf1-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="f1cf1-114">Используйте необходимые квалификаторы, чтобы определить расположение поставщика реестра и расположение соответствующего раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="f1cf1-115">Поставщик системного реестра использует три квалификатора для определения расположения различных классов, поставщиков и записей реестра.</span><span class="sxs-lookup"><span data-stu-id="f1cf1-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="f1cf1-116">Дополнительные сведения см. [в разделе Определение класса реестра с квалификаторами](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="f1cf1-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



