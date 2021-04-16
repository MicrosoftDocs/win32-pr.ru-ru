---
description: Установщик устанавливает значение свойства «скользящее» в строковое представление идентификатора безопасности (SID) пользователя, запустившего установку. Дополнительные сведения см. в разделе структуры авторизации.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Свойство "значение"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651931"
---
# <a name="usersid-property"></a><span data-ttu-id="227e9-104">Свойство "значение"</span><span class="sxs-lookup"><span data-stu-id="227e9-104">UserSID property</span></span>

<span data-ttu-id="227e9-105">Установщик устанавливает **значение свойства «скользящее» в** строковое представление идентификатора безопасности (SID) пользователя, запустившего установку.</span><span class="sxs-lookup"><span data-stu-id="227e9-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="227e9-106">Дополнительные сведения см. в разделе [структуры авторизации](../secauthz/authorization-structures.md).</span><span class="sxs-lookup"><span data-stu-id="227e9-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="227e9-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="227e9-107">Default Value</span></span>

<span data-ttu-id="227e9-108">Нет.</span><span class="sxs-lookup"><span data-stu-id="227e9-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="227e9-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="227e9-109">Remarks</span></span>

<span data-ttu-id="227e9-110">Установщик Windows задать это свойство в Windows 2000, Windows XP и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="227e9-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="227e9-111">Это свойство не определено во всех других операционных системах.</span><span class="sxs-lookup"><span data-stu-id="227e9-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="227e9-112">Обратите внимание, что это свойство имеет специальный атрибут, который можно получить из отложенного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="227e9-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="227e9-113">Пользовательское действие, выполняемое с повышенными привилегиями **, по-** прежнему может возвращать идентификатор SID пользователя в свойстве "скользящее".</span><span class="sxs-lookup"><span data-stu-id="227e9-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="227e9-114">Дополнительные сведения см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="227e9-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="227e9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="227e9-115">Requirements</span></span>



| <span data-ttu-id="227e9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="227e9-116">Requirement</span></span> | <span data-ttu-id="227e9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="227e9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="227e9-118">Версия</span><span class="sxs-lookup"><span data-stu-id="227e9-118">Version</span></span><br/> | <span data-ttu-id="227e9-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="227e9-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="227e9-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="227e9-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="227e9-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="227e9-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="227e9-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="227e9-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="227e9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="227e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="227e9-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="227e9-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 
