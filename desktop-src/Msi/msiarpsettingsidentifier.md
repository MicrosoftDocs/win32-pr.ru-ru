---
description: Свойство МСИАРПСЕТТИНГСИДЕНТИФИЕР содержит разделенный точками с запятой список расположений реестра, в которых приложение хранит параметры и предпочтения пользователя.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: МСИАРПСЕТТИНГСИДЕНТИФИЕР, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669084"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="d59b6-103">МСИАРПСЕТТИНГСИДЕНТИФИЕР, свойство</span><span class="sxs-lookup"><span data-stu-id="d59b6-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="d59b6-104">Свойство **мсиарпсеттингсидентифиер** содержит разделенный точками с запятой список расположений реестра, в которых приложение хранит параметры и предпочтения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d59b6-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="d59b6-105">Во время обновления операционной системы программа установки может использовать эти сведения для улучшения работы пользователей, выполняющих миграцию приложений.</span><span class="sxs-lookup"><span data-stu-id="d59b6-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="d59b6-106">Значением свойства **мсиарпсеттингсидентифиер** является литеральный текст, содержащий список расположений реестра, в которых приложение хранит свои параметры.</span><span class="sxs-lookup"><span data-stu-id="d59b6-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="d59b6-107">Значение может указывать несколько возможных расположений в реестре.</span><span class="sxs-lookup"><span data-stu-id="d59b6-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="d59b6-108">Разделяйте несколько расположений реестра с помощью точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="d59b6-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="d59b6-109">Параметры приложения обычно хранятся в кустах реестра **HKCU** или **HKLM** в формате " *\\ \\ версия приложения компании*".</span><span class="sxs-lookup"><span data-stu-id="d59b6-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="d59b6-110">В следующем примере показано возможное значение для свойства **мсиарпсеттингсидентифиер** .</span><span class="sxs-lookup"><span data-stu-id="d59b6-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="d59b6-111">*MyCompany \\ аппсуите \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="d59b6-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="d59b6-112">Это свойство является необязательным и может быть задано в таблице [свойств](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d59b6-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="d59b6-113">Если это свойство отображается в таблице свойств, значение не должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="d59b6-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d59b6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d59b6-114">Requirements</span></span>



| <span data-ttu-id="d59b6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d59b6-115">Requirement</span></span> | <span data-ttu-id="d59b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d59b6-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d59b6-117">Версия</span><span class="sxs-lookup"><span data-stu-id="d59b6-117">Version</span></span><br/> | <span data-ttu-id="d59b6-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d59b6-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d59b6-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d59b6-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d59b6-120">Установщик Windows 4,5 в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d59b6-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d59b6-121">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d59b6-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d59b6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d59b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d59b6-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="d59b6-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d59b6-124">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="d59b6-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




