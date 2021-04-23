---
description: Присвойте свойству МСИУСЕРЕАЛАДМИНДЕТЕКТИОН значение 1, чтобы запросить, что установщик использует фактические сведения о пользователе при задании свойства AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: МСИУСЕРЕАЛАДМИНДЕТЕКТИОН, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679605"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="c9412-103">МСИУСЕРЕАЛАДМИНДЕТЕКТИОН, свойство</span><span class="sxs-lookup"><span data-stu-id="c9412-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="c9412-104">Присвойте свойству **мсиусереаладминдетектион** значение 1, чтобы запросить, что установщик использует фактические сведения о пользователе при задании свойства [**AdminUser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="c9412-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="c9412-105">При работе в Windows Vista [**привилегированные**](privileged.md) и **AdminUser** совпадают.</span><span class="sxs-lookup"><span data-stu-id="c9412-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="c9412-106">Авторы должны использовать **привилегированное** свойство в новых пакетах.</span><span class="sxs-lookup"><span data-stu-id="c9412-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="c9412-107">Устаревшие пакеты, для которых требуются разные свойства **privileged** и **AdminUser** , могут восстановить разницу, задав свойство **мсиусереаладминдетектион** .</span><span class="sxs-lookup"><span data-stu-id="c9412-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9412-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c9412-108">Requirements</span></span>



| <span data-ttu-id="c9412-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c9412-109">Requirement</span></span> | <span data-ttu-id="c9412-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c9412-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9412-111">Версия</span><span class="sxs-lookup"><span data-stu-id="c9412-111">Version</span></span><br/> | <span data-ttu-id="c9412-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9412-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9412-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9412-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9412-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c9412-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9412-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c9412-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9412-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9412-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c9412-117">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="c9412-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




