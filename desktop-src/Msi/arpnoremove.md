---
description: Установка свойства АРПНОРЕМОВЕ отключает функцию "Установка и удаление программ" на панели управления, которая удаляет продукт.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: АРПНОРЕМОВЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668503"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="6f6eb-103">АРПНОРЕМОВЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="6f6eb-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="6f6eb-104">Установка свойства **арпноремове** отключает функцию " **Установка и удаление программ** " на **панели управления** , которая удаляет продукт.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="6f6eb-105">Для Windows 2000 эта кнопка отключает кнопку **Удалить** для продукта из окна **Установка и удаление программ** **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="6f6eb-106">В более ранних операционных системах это действие приводит к удалению продукта из списка установленных продуктов в **панели управления** **Установка и удаление программ** .</span><span class="sxs-lookup"><span data-stu-id="6f6eb-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="6f6eb-107">Если задано свойство **арпноремове** , [действие регистерпродукт](registerproduct-action.md) записывает значение "Удалить" в раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="6f6eb-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="6f6eb-108">**HKLM** \\ **Программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Удалить** \\ **{*ключ продукта*}**</span><span class="sxs-lookup"><span data-stu-id="6f6eb-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="6f6eb-109">Установка свойства **арпноремове** предотвращает запись значения унинсталлстринг в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="6f6eb-110">Значение Унисталлстринг — это Командная строка для удаления продукта, а не перенастройка продукта.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6eb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f6eb-111">Remarks</span></span>

<span data-ttu-id="6f6eb-112">Например, это свойство можно задать во время преобразования настройки, чтобы запретить пользователям удалять настройку администратора.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6eb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6f6eb-113">Requirements</span></span>



| <span data-ttu-id="6f6eb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6f6eb-114">Requirement</span></span> | <span data-ttu-id="6f6eb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6f6eb-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6eb-116">Версия</span><span class="sxs-lookup"><span data-stu-id="6f6eb-116">Version</span></span><br/> | <span data-ttu-id="6f6eb-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6f6eb-118">Установщик Windows 4,0 или установщик Windows 4,5 или более поздней версии в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="6f6eb-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6f6eb-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6f6eb-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f6eb-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6f6eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6eb-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f6eb-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




