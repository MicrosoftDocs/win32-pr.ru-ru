---
description: Предварительно выбранное свойство указывает, что компоненты уже выбраны и что диалоговое окно выбора не должно отображаться. Условные выражения, которые зависят от того, установлены ли уже компоненты, используют это значение.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Предвыбранное свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652133"
---
# <a name="preselected-property"></a><span data-ttu-id="06075-103">Предвыбранное свойство</span><span class="sxs-lookup"><span data-stu-id="06075-103">Preselected property</span></span>

<span data-ttu-id="06075-104">Предварительно **выбранное** свойство указывает, что компоненты уже выбраны и что диалоговое окно выбора не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="06075-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="06075-105">Условные выражения, которые зависят от того, установлены ли уже компоненты, используют это значение.</span><span class="sxs-lookup"><span data-stu-id="06075-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="06075-106">Например, свойство можно использовать для подавления диалоговых окон, в которых используются возможности выбора компонентов при возобновлении приостановленной установки.</span><span class="sxs-lookup"><span data-stu-id="06075-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="06075-107">Установщик задает для свойства предварительно **выбранных** значений значение "1" во время возобновления приостановленной установки или при указании любого из следующих свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="06075-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="06075-108">Если предварительно **выбранное** свойство было установлено в 1, то установщик не использует [таблицу условий](condition-table.md) для вычисления выбранных компонентов.</span><span class="sxs-lookup"><span data-stu-id="06075-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="06075-109">Компоненты устанавливаются на основе следующих свойств.</span><span class="sxs-lookup"><span data-stu-id="06075-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="06075-110">Установщик всегда вычисляет эти свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="06075-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="06075-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="06075-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="06075-112">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="06075-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="06075-113">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="06075-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="06075-114">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="06075-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="06075-115">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="06075-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="06075-116">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="06075-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="06075-117">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="06075-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="06075-118">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="06075-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="06075-119">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="06075-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="06075-120">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="06075-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="06075-121">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="06075-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="06075-122">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="06075-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="06075-123">Требования</span><span class="sxs-lookup"><span data-stu-id="06075-123">Requirements</span></span>



| <span data-ttu-id="06075-124">Требование</span><span class="sxs-lookup"><span data-stu-id="06075-124">Requirement</span></span> | <span data-ttu-id="06075-125">Значение</span><span class="sxs-lookup"><span data-stu-id="06075-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06075-126">Версия</span><span class="sxs-lookup"><span data-stu-id="06075-126">Version</span></span><br/> | <span data-ttu-id="06075-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="06075-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="06075-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="06075-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="06075-129">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06075-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="06075-130">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="06075-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06075-131">См. также</span><span class="sxs-lookup"><span data-stu-id="06075-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06075-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="06075-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




