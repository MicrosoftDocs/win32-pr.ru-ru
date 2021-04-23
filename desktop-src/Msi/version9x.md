---
description: 'Свойство Version9X предоставляет номер версии для версий операционной системы Windows 9x. Значение этого свойства является целым числом: MajorVersion \* 100 + minorversion.'
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Version9X, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df599629fdf978837a8f53df7d1faa4f476db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674928"
---
# <a name="version9x-property"></a><span data-ttu-id="3e8e9-103">Version9X, свойство</span><span class="sxs-lookup"><span data-stu-id="3e8e9-103">Version9X property</span></span>

<span data-ttu-id="3e8e9-104">Свойство **Version9X** предоставляет номер версии для версий операционной системы Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-104">The **Version9X** property gives the version number for 9x versions of Windows operating systems.</span></span>

<span data-ttu-id="3e8e9-105">Значение этого свойства является целым числом: MajorVersion \* 100 + minorversion.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-105">The value of this property is an integer: MajorVersion \* 100 + MinorVersion.</span></span> <span data-ttu-id="3e8e9-106">Если операционная система не является версией 9x, свойство остается неопределенным.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-106">The property remains undefined if the operating system is not a 9x version.</span></span> <span data-ttu-id="3e8e9-107">Дополнительные сведения см. в разделе [значения свойств операционной системы](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="3e8e9-107">For more information, see [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e8e9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e8e9-108">Remarks</span></span>

<span data-ttu-id="3e8e9-109">Выражения условий могут проверять версию с помощью имени свойства или проверить версию с помощью оператора сравнения.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-109">Condition expressions can test for the version by using the property name or may verify the version by using a comparison operator.</span></span>

<span data-ttu-id="3e8e9-110">В именах всех свойств учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-110">All property names are case-sensitive.</span></span> <span data-ttu-id="3e8e9-111">Обратите внимание, что X в имени **Version9X** является прописной буквой.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-111">Note that the X in the name **Version9X** is uppercase.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8e9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3e8e9-112">Requirements</span></span>



| <span data-ttu-id="3e8e9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3e8e9-113">Requirement</span></span> | <span data-ttu-id="3e8e9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3e8e9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8e9-115">Версия</span><span class="sxs-lookup"><span data-stu-id="3e8e9-115">Version</span></span><br/> | <span data-ttu-id="3e8e9-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3e8e9-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3e8e9-118">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e8e9-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3e8e9-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3e8e9-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e8e9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3e8e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8e9-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e8e9-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




