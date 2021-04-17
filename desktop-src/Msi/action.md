---
description: Для свойства ACTION можно задать следующие значения.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Свойство ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652034"
---
# <a name="action-property"></a><span data-ttu-id="c38fa-103">Свойство ACTION</span><span class="sxs-lookup"><span data-stu-id="c38fa-103">ACTION property</span></span>

<span data-ttu-id="c38fa-104">Для свойства **Action** можно задать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c38fa-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="c38fa-105">Значение</span><span class="sxs-lookup"><span data-stu-id="c38fa-105">Value</span></span>



| <span data-ttu-id="c38fa-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c38fa-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="c38fa-107">Значение</span><span class="sxs-lookup"><span data-stu-id="c38fa-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="c38fa-108"><dt>**ВЗНОС**</dt></span><span class="sxs-lookup"><span data-stu-id="c38fa-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="c38fa-109">Действие установки</span><span class="sxs-lookup"><span data-stu-id="c38fa-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="c38fa-110"><dt>**РЕКЛАМИРОВАТЬ**</dt></span><span class="sxs-lookup"><span data-stu-id="c38fa-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="c38fa-111">Действие объявления</span><span class="sxs-lookup"><span data-stu-id="c38fa-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="c38fa-112"><dt>**ГРУППЫ**</dt></span><span class="sxs-lookup"><span data-stu-id="c38fa-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="c38fa-113">Действие администратора</span><span class="sxs-lookup"><span data-stu-id="c38fa-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="c38fa-114">Свойство **Action** определяет, какое действие следует выполнить, если для [**Мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) или [**метода DoAction**](session-doaction.md)задано имя действия null.</span><span class="sxs-lookup"><span data-stu-id="c38fa-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="c38fa-115">Если для свойства **Action** не определено значение, установщик вызывает [действие Install](install-action.md).</span><span class="sxs-lookup"><span data-stu-id="c38fa-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c38fa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c38fa-116">Requirements</span></span>



| <span data-ttu-id="c38fa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c38fa-117">Requirement</span></span> | <span data-ttu-id="c38fa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c38fa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38fa-119">Версия</span><span class="sxs-lookup"><span data-stu-id="c38fa-119">Version</span></span><br/> | <span data-ttu-id="c38fa-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c38fa-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c38fa-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c38fa-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c38fa-122">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c38fa-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c38fa-123">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c38fa-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c38fa-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c38fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38fa-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="c38fa-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




