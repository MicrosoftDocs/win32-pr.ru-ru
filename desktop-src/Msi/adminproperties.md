---
description: Админпропертиес должен быть создан в таблице свойств.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Админпропертиес, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669465"
---
# <a name="adminproperties-property"></a><span data-ttu-id="c196a-103">Админпропертиес, свойство</span><span class="sxs-lookup"><span data-stu-id="c196a-103">AdminProperties property</span></span>

<span data-ttu-id="c196a-104">**Админпропертиес** должен быть создан в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c196a-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="c196a-105">Значение **админпропертиес** представляет собой список имен свойств, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="c196a-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="c196a-106">Установщик сохраняет значения этих перечисленных свойств во время [административной установки](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c196a-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="c196a-107">При установке пользователей из административного образа при установке используются сохраненные значения свойств, а не значения в файле MSI.</span><span class="sxs-lookup"><span data-stu-id="c196a-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="c196a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c196a-108">Remarks</span></span>

<span data-ttu-id="c196a-109">Имена свойств в списке могут быть прописными и строчными буквами (закрытыми свойствами) или прописными (открытыми свойствами).</span><span class="sxs-lookup"><span data-stu-id="c196a-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="c196a-110">Это свойство не должно заканчиваться точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="c196a-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="c196a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c196a-111">Requirements</span></span>



| <span data-ttu-id="c196a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c196a-112">Requirement</span></span> | <span data-ttu-id="c196a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c196a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c196a-114">Версия</span><span class="sxs-lookup"><span data-stu-id="c196a-114">Version</span></span><br/> | <span data-ttu-id="c196a-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c196a-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c196a-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c196a-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c196a-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c196a-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c196a-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c196a-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c196a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c196a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c196a-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="c196a-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




