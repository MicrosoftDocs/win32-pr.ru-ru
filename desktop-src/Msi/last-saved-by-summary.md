---
description: Установщик устанавливает последнее сохраненное свойство по значению, которое зависит от того, является ли это пакетом установки, преобразованием или пакетом исправлений. В пакете установки установщик задает для этого свойства значение свойства LogonUser во время административной установки. Разработчики средств редактирования баз данных могут использовать это свойство в процессе разработки, чтобы отслеживанию последнего пользователя для изменения базы данных установки. Это свойство должно иметь значение NULL в конечной базе данных доставки. Установщик никогда не использует это свойство, и пользователь не должен изменять его. В преобразовании это свойство сводки содержит ИДЕНТИФИКАТОРы платформы и языка, которые должна иметь база данных после преобразования. Свойство указывает, что должна быть задана сводка по шаблону в новой базе данных. В пакете исправлений это свойство сводки содержит список, разделенный точкой с запятой, для преобразования имен подхранилищ в том порядке, в котором они были применены этим исправлением.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Последнее сохранение по свойству Summary
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689088"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="122e5-107">Последнее сохранение по свойству Summary</span><span class="sxs-lookup"><span data-stu-id="122e5-107">Last Saved By Summary property</span></span>

<span data-ttu-id="122e5-108">Установщик устанавливает **последнее сохраненное свойство по** значению, которое зависит от того, является ли это пакетом установки, преобразованием или пакетом исправлений.</span><span class="sxs-lookup"><span data-stu-id="122e5-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="122e5-109">В пакете установки установщик задает для этого свойства значение свойства [**LogonUser**](logonuser.md) во время [административной установки](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="122e5-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="122e5-110">Разработчики средств редактирования баз данных могут использовать это свойство в процессе разработки, чтобы отслеживанию последнего пользователя для изменения базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="122e5-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="122e5-111">Это свойство должно иметь значение NULL в конечной базе данных доставки.</span><span class="sxs-lookup"><span data-stu-id="122e5-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="122e5-112">Установщик никогда не использует это свойство, и пользователь не должен изменять его.</span><span class="sxs-lookup"><span data-stu-id="122e5-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="122e5-113">В преобразовании это свойство сводки содержит ИДЕНТИФИКАТОРы платформы и языка, которые должна иметь база данных после преобразования.</span><span class="sxs-lookup"><span data-stu-id="122e5-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="122e5-114">Свойство указывает, что должна быть задана [**Сводка по шаблону**](template-summary.md) в новой базе данных.</span><span class="sxs-lookup"><span data-stu-id="122e5-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="122e5-115">В пакете исправлений это свойство сводки содержит список, разделенный точкой с запятой, для преобразования имен подхранилищ в том порядке, в котором они были применены этим исправлением.</span><span class="sxs-lookup"><span data-stu-id="122e5-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="122e5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="122e5-116">Requirements</span></span>



| <span data-ttu-id="122e5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="122e5-117">Requirement</span></span> | <span data-ttu-id="122e5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="122e5-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122e5-119">Версия</span><span class="sxs-lookup"><span data-stu-id="122e5-119">Version</span></span><br/> | <span data-ttu-id="122e5-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="122e5-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="122e5-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="122e5-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="122e5-122">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="122e5-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="122e5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="122e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122e5-124">Описания свойств сводки</span><span class="sxs-lookup"><span data-stu-id="122e5-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




