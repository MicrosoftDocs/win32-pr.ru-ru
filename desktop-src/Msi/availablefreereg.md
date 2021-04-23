---
description: Свойство АВАИЛАБЛЕФРИРЕГ указывает в килобайтах общее свободное пространство, доступное в реестре, после вызова действия Аллокатерегистриспаце. Максимальное значение свойства АВАИЛАБЛЕФРИРЕГ — 2000000 КБ. Это свойство задается только в Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: АВАИЛАБЛЕФРИРЕГ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652089"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="6199d-103">АВАИЛАБЛЕФРИРЕГ, свойство</span><span class="sxs-lookup"><span data-stu-id="6199d-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="6199d-104">Свойство **аваилаблефрирег** указывает в килобайтах общее свободное пространство, доступное в реестре, после вызова [действия аллокатерегистриспаце](allocateregistryspace-action.md).</span><span class="sxs-lookup"><span data-stu-id="6199d-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="6199d-105">Максимальное значение свойства **аваилаблефрирег** — 2000000 КБ.</span><span class="sxs-lookup"><span data-stu-id="6199d-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="6199d-106">Это свойство задается только в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6199d-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="6199d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6199d-107">Remarks</span></span>

<span data-ttu-id="6199d-108">Свойству **аваилаблефрирег** должно быть присвоено достаточное значение, чтобы обеспечить достаточное пространство в реестре для всех сведений о регистрации, добавляемых в установку.</span><span class="sxs-lookup"><span data-stu-id="6199d-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="6199d-109">Минимальное значение, необходимое для обеспечения достаточного места, зависит от того, где находится [действие аллокатерегистриспаце](allocateregistryspace-action.md) в последовательности действий, так как установщик автоматически увеличивает пространство при регистрации данных в [реестре](registry-table.md), [классе](class-table.md), [селфрег](selfreg-table.md), [расширении](extension-table.md), [MIME](mime-table.md)и в таблицах [команд](verb-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6199d-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="6199d-110">Установщик не увеличивает общий объем пространства реестра до значения, указанного параметром **аваилаблефрирег** , до достижения аллокатерегистриспаце в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="6199d-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="6199d-111">Если Аллокатерегистриспаце является одним из первых действий в последовательности действий, **аваилаблефрирег** следует задать общее пространство, необходимое для сведений о регистрации в таблице реестра, таблицу классов, таблицу TypeLib, таблицу селфрег, таблицу расширений, таблицу MIME, таблицу команд, регистрацию [настраиваемых действий](custom-actions.md) , самостоятельную регистрацию и любые другие данные реестра, записанные во время установки.</span><span class="sxs-lookup"><span data-stu-id="6199d-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="6199d-112">Значение **аваилаблефрирег** — это общий объем информации, добавляемой при установке, и обеспечивает достаточно места во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="6199d-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="6199d-113">Это также самый распространенный случай.</span><span class="sxs-lookup"><span data-stu-id="6199d-113">This is also the most common case.</span></span>

<span data-ttu-id="6199d-114">Если действие Аллокатерегистриспаце может быть создано в последовательности действий после всех [стандартных действий](standard-actions.md) , которые записывают регистрационные данные, такие как [вритерегистривалуес](writeregistryvalues-action.md) и [регистерклассинфо](registerclassinfo-action.md), то значение **аваилаблефрирег** должно быть установлено только на пространство, необходимое для регистрации пользовательских действий, регистрации библиотек типов и других сведений, которые еще не зарегистрированы в таблицах.</span><span class="sxs-lookup"><span data-stu-id="6199d-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="6199d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6199d-115">Requirements</span></span>



| <span data-ttu-id="6199d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6199d-116">Requirement</span></span> | <span data-ttu-id="6199d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6199d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6199d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6199d-118">Version</span></span><br/> | <span data-ttu-id="6199d-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6199d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6199d-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6199d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6199d-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6199d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6199d-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6199d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6199d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6199d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6199d-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="6199d-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




