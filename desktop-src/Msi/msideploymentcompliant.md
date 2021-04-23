---
description: Свойство МСИДЕПЛОЙМЕНТКОМПЛИАНТ можно задать, чтобы указать установщику, что пакет был создан и проверен на соответствие контролю учетных записей (UAC) в Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: МСИДЕПЛОЙМЕНТКОМПЛИАНТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652014"
---
# <a name="msideploymentcompliant-property"></a><span data-ttu-id="511a6-103">МСИДЕПЛОЙМЕНТКОМПЛИАНТ, свойство</span><span class="sxs-lookup"><span data-stu-id="511a6-103">MSIDEPLOYMENTCOMPLIANT property</span></span>

<span data-ttu-id="511a6-104">Свойство **мсидеплойменткомплиант** можно задать, чтобы указать установщику, что пакет был создан и проверен на соответствие [*контролю учетных записей*](u-gly.md) (UAC) в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="511a6-104">The **MSIDEPLOYMENTCOMPLIANT** property can be set to indicate to the installer that the package has been authored and tested to comply with [*User Account Control*](u-gly.md) (UAC) in Windows Vista.</span></span> <span data-ttu-id="511a6-105">Если это свойство не задано, установщик определит, соответствует ли пакет требованиям UAC в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="511a6-105">If this property is not set, the installer will determine whether the package complies with UAC on Windows Vista.</span></span>

<span data-ttu-id="511a6-106">Дополнительные сведения о контроле учетных записей и установщик Windows см. в разделе [использование установщик Windows с UAC](using-windows-installer-with-uac.md) и [рекомендации по пакетам](guidelines-for-packages.md).</span><span class="sxs-lookup"><span data-stu-id="511a6-106">For more information about UAC and Windows Installer, see [Using Windows Installer with UAC](using-windows-installer-with-uac.md) and [Guidelines for Packages](guidelines-for-packages.md).</span></span>

<span data-ttu-id="511a6-107">**Установщик Windows 3,1, установщик Windows 3,0 и установщик Windows 2,0:** Это свойство не учитывается.</span><span class="sxs-lookup"><span data-stu-id="511a6-107">**Windows Installer 3.1, Windows Installer 3.0 and Windows Installer 2.0:** This property is ignored.</span></span> <span data-ttu-id="511a6-108">Это свойство используется только установщик Windows 4,0 в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="511a6-108">This property is only used by Windows Installer 4.0 in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="511a6-109">Требования</span><span class="sxs-lookup"><span data-stu-id="511a6-109">Requirements</span></span>



| <span data-ttu-id="511a6-110">Требование</span><span class="sxs-lookup"><span data-stu-id="511a6-110">Requirement</span></span> | <span data-ttu-id="511a6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="511a6-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="511a6-112">Версия</span><span class="sxs-lookup"><span data-stu-id="511a6-112">Version</span></span><br/> | <span data-ttu-id="511a6-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="511a6-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="511a6-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="511a6-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="511a6-115">Сведения о минимальном пакете обновления, требуемом для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="511a6-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="511a6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="511a6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511a6-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="511a6-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="511a6-118">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="511a6-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




