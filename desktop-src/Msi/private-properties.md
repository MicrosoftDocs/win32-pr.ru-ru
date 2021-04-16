---
description: Закрытые свойства используются для внутренних целей установщика, и их значения должны вводиться автором пакета установки или устанавливаться установщиком во время установки на значения, определенные операционной средой.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Закрытые свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651000"
---
# <a name="private-properties"></a><span data-ttu-id="aec81-103">Закрытые свойства</span><span class="sxs-lookup"><span data-stu-id="aec81-103">Private Properties</span></span>

<span data-ttu-id="aec81-104">Закрытые свойства используются для внутренних целей установщика, и их значения должны вводиться автором пакета установки или устанавливаться установщиком во время установки на значения, определенные операционной средой.</span><span class="sxs-lookup"><span data-stu-id="aec81-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="aec81-105">Единственный способ взаимодействия пользователя с закрытыми свойствами — [Управление событиями](control-events.md) в созданном пользователем интерфейсе пакета.</span><span class="sxs-lookup"><span data-stu-id="aec81-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="aec81-106">Имена закрытых свойств должны включать строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="aec81-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="aec81-107">См. раздел [ограничения имен свойств](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="aec81-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="aec81-108">Закрытые свойства обычно описывают операционную среду.</span><span class="sxs-lookup"><span data-stu-id="aec81-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="aec81-109">Например, если установка выполняется на платформе Windows, установщик устанавливает для свойства [**виндовсфолдер**](windowsfolder.md) значение, указанное в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="aec81-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="aec81-110">Значения закрытых свойств не могут быть переопределены в командной строке.</span><span class="sxs-lookup"><span data-stu-id="aec81-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="aec81-111">Чтобы удалить закрытое свойство из установки, оставьте его из [таблицы свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="aec81-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="aec81-112">В Windows XP и Windows 2000 нельзя задать свойство Private на этапе пользовательского интерфейса установки, а затем передать значение на фазу выполнения.</span><span class="sxs-lookup"><span data-stu-id="aec81-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="aec81-113">Список всех стандартных закрытых свойств, используемых установщиком, см. в разделе [Справочник по свойствам](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="aec81-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="aec81-114">Можно определить пользовательское закрытое свойство, введя имя свойства и начальное значение в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="aec81-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="aec81-115">Имена закрытых свойств должны всегда содержать строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="aec81-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec81-116">См. также</span><span class="sxs-lookup"><span data-stu-id="aec81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec81-117">Открытые свойства</span><span class="sxs-lookup"><span data-stu-id="aec81-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



