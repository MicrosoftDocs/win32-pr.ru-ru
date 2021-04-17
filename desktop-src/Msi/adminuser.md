---
description: Установщик задает это свойство, если у пользователя есть права администратора.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652278"
---
# <a name="adminuser-property"></a><span data-ttu-id="4295c-103">AdminUser, свойство</span><span class="sxs-lookup"><span data-stu-id="4295c-103">AdminUser property</span></span>

<span data-ttu-id="4295c-104">Установщик задает это свойство, если у пользователя есть права администратора.</span><span class="sxs-lookup"><span data-stu-id="4295c-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="4295c-105">**Windows Server 2008 и Windows Vista:** Свойство **AdminUser** совпадает с [**привилегированным**](privileged.md) свойством.</span><span class="sxs-lookup"><span data-stu-id="4295c-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="4295c-106">Авторы должны использовать **привилегированное** свойство.</span><span class="sxs-lookup"><span data-stu-id="4295c-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="4295c-107">Установщик задает эти свойства, если пользователь имеет права администратора, если приложение назначено системным администратором или если для политики пользователя и компьютера AlwaysInstallElevated задано значение true.</span><span class="sxs-lookup"><span data-stu-id="4295c-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="4295c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4295c-108">Remarks</span></span>

<span data-ttu-id="4295c-109">Различия между этими свойствами могут быть использованы в некоторых устаревших пакетах.</span><span class="sxs-lookup"><span data-stu-id="4295c-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="4295c-110">Например, **AdminUser** может использоваться вместо [**привилегированных**](privileged.md) операторов в условных инструкциях, так как установщик задает свойство **AdminUser** только в том случае, если пользователь является администратором.</span><span class="sxs-lookup"><span data-stu-id="4295c-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="4295c-111">Установщик задает **привилегированное** свойство, если пользователь является администратором, или, если политика позволяет пользователю устанавливать с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="4295c-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="4295c-112">**Windows Server 2008 и Windows Vista:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4295c-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="4295c-113">[**Привилегированные**](privileged.md) и **AdminUser** одинаковы.</span><span class="sxs-lookup"><span data-stu-id="4295c-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="4295c-114">Пакеты, требующие различных свойств **privileged** и **AdminUser** , могут восстановить разницу, задав свойство [**мсиусереаладминдетектион**](msiuserealadmindetection.md) .</span><span class="sxs-lookup"><span data-stu-id="4295c-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="4295c-115">Дополнительные сведения см. в разделе [Установка пакета с повышенными привилегиями для свойства без прав администратора](installing-a-package-with-elevated-privileges-for-a-non-admin.md)и [**привилегированного**](privileged.md) доступа.</span><span class="sxs-lookup"><span data-stu-id="4295c-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4295c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4295c-116">Requirements</span></span>



| <span data-ttu-id="4295c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4295c-117">Requirement</span></span> | <span data-ttu-id="4295c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4295c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4295c-119">Версия</span><span class="sxs-lookup"><span data-stu-id="4295c-119">Version</span></span><br/> | <span data-ttu-id="4295c-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4295c-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4295c-121">Установщик Windows 4,0 или установщик Windows 4,5 в Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4295c-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="4295c-122">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4295c-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4295c-123">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4295c-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4295c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4295c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4295c-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="4295c-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




