---
description: Установленное свойство задается только в том случае, если продукт установлен для каждого компьютера или для текущего пользователя.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Установленное свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652062"
---
# <a name="installed-property"></a><span data-ttu-id="a48ee-103">Установленное свойство</span><span class="sxs-lookup"><span data-stu-id="a48ee-103">Installed property</span></span>

<span data-ttu-id="a48ee-104">**Установленное** свойство задается только в том случае, если продукт установлен для каждого компьютера или для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a48ee-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="a48ee-105">Это свойство не задано, если продукт установлен для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a48ee-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="a48ee-106">**Установленное** свойство может использоваться в условных выражениях для определения того, установлен ли продукт для каждого компьютера или для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a48ee-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="a48ee-107">Например, свойство может использоваться в условном столбце таблицы последовательностей или для различения первой установки и установки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a48ee-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="a48ee-108">Чтобы определить, установлен ли продукт для другого пользователя, проверьте свойство [**продуктстате**](productstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a48ee-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="a48ee-109">Значение свойства [**ProductVersion**](productversion.md) — это версия продукта в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="a48ee-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48ee-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a48ee-110">Requirements</span></span>



| <span data-ttu-id="a48ee-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a48ee-111">Requirement</span></span> | <span data-ttu-id="a48ee-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a48ee-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48ee-113">Версия</span><span class="sxs-lookup"><span data-stu-id="a48ee-113">Version</span></span><br/> | <span data-ttu-id="a48ee-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a48ee-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a48ee-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a48ee-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a48ee-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a48ee-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a48ee-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a48ee-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a48ee-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a48ee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48ee-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="a48ee-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




