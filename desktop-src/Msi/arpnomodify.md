---
description: Установка свойства АРПНОМОДИФИ отключает функцию "Установка и удаление программ" на панели управления, которая изменяет продукт.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: АРПНОМОДИФИ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651892"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="d93e8-103">АРПНОМОДИФИ, свойство</span><span class="sxs-lookup"><span data-stu-id="d93e8-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="d93e8-104">Установка свойства **арпномодифи** отключает функцию "Установка и удаление программ" на панели управления, которая изменяет продукт.</span><span class="sxs-lookup"><span data-stu-id="d93e8-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="d93e8-105">Для Windows 2000 это отключает кнопку " **изменить** " для продукта в окне " **Установка и удаление программ** " **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="d93e8-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="d93e8-106">В более ранних операционных системах при нажатии кнопки « **Установка и удаление программ** » продукт удаляется, а не заменяется мастером режима обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d93e8-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="d93e8-107">Если задано свойство **арпномодифи** , [действие регистерпродукт](registerproduct-action.md) записывает значение "неизменного" в раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="d93e8-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="d93e8-108">**HKLM** \\ **Программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Удалить** \\ **{*ключ продукта*}**</span><span class="sxs-lookup"><span data-stu-id="d93e8-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="d93e8-109">Если свойство **арпномодифи** задано и свойство [**арпноремове**](arpnoremove.md) не задано, действие регистерпродукт также записывает значение унинсталлстринг в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d93e8-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="d93e8-110">Значение Унисталлстринг — это Командная строка для удаления продукта, а не перенастройка продукта.</span><span class="sxs-lookup"><span data-stu-id="d93e8-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="d93e8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d93e8-111">Remarks</span></span>

<span data-ttu-id="d93e8-112">В Windows 2000 эта кнопка отключает кнопку **изменить** для продукта в окне **Установка и удаление программ** **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="d93e8-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="d93e8-113">Это свойство можно задать с помощью преобразования настройки, чтобы запретить пользователям изменять настройки администратора с помощью элемента " **Установка и удаление программ**".</span><span class="sxs-lookup"><span data-stu-id="d93e8-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="d93e8-114">Это свойство влияет только на компонент " **Установка и удаление программ**".</span><span class="sxs-lookup"><span data-stu-id="d93e8-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93e8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d93e8-115">Requirements</span></span>



| <span data-ttu-id="d93e8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d93e8-116">Requirement</span></span> | <span data-ttu-id="d93e8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d93e8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93e8-118">Версия</span><span class="sxs-lookup"><span data-stu-id="d93e8-118">Version</span></span><br/> | <span data-ttu-id="d93e8-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d93e8-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d93e8-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d93e8-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d93e8-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d93e8-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d93e8-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d93e8-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d93e8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d93e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e8-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="d93e8-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d93e8-125">Пример преобразования настройки</span><span class="sxs-lookup"><span data-stu-id="d93e8-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




