---
description: Задание этого свойства аналогично установке политики политики Трансформсатсаурце, за исключением того, что область отличается.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: ТРАНСФОРМСАТСАУРЦЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679932"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="70673-103">ТРАНСФОРМСАТСАУРЦЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="70673-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="70673-104">Задание этого свойства аналогично установке политики [политики трансформсатсаурце](transformsatsource-policy.md) , за исключением того, что область отличается.</span><span class="sxs-lookup"><span data-stu-id="70673-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="70673-105">Настройка политики Трансформсатсаурце применяется ко всем пакетам, установленным указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="70673-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="70673-106">Установка свойства **трансформсатсаурце** применяется к пакету независимо от пользователей.</span><span class="sxs-lookup"><span data-stu-id="70673-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="70673-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70673-107">Remarks</span></span>

<span data-ttu-id="70673-108">Установщик Windows интерпретирует свойство **трансформсатсаурце** , как будто оно было свойством [**трансформссекуре**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="70673-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="70673-109">Если в свойстве [**TRANSFORMS**](transforms.md) передается флаг @, установщик Windows обрабатывает преобразования в списке как [преобразования с защитой по источнику](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="70673-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70673-110">Требования</span><span class="sxs-lookup"><span data-stu-id="70673-110">Requirements</span></span>



| <span data-ttu-id="70673-111">Требование</span><span class="sxs-lookup"><span data-stu-id="70673-111">Requirement</span></span> | <span data-ttu-id="70673-112">Значение</span><span class="sxs-lookup"><span data-stu-id="70673-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70673-113">Версия</span><span class="sxs-lookup"><span data-stu-id="70673-113">Version</span></span><br/> | <span data-ttu-id="70673-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70673-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="70673-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70673-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="70673-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70673-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="70673-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="70673-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70673-118">См. также</span><span class="sxs-lookup"><span data-stu-id="70673-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70673-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="70673-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




