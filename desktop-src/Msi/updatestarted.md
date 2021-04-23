---
description: Установщик задает свойство Упдатестартед, когда изменения в системе приступили к установке, включая возобновление приостановленной установки. В инструкциях условия пользовательского интерфейса это значение используется для выбора диалогового окна.
ms.assetid: aebc4a20-22b9-4a81-abed-1fed61b880da
title: Упдатестартед, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99561d17bf6fcb251f1acd7ac0d30ed5c1682997
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652147"
---
# <a name="updatestarted-property"></a><span data-ttu-id="74e0e-103">Упдатестартед, свойство</span><span class="sxs-lookup"><span data-stu-id="74e0e-103">UpdateStarted property</span></span>

<span data-ttu-id="74e0e-104">Установщик задает свойство **упдатестартед** , когда изменения в системе приступили к установке, включая возобновление приостановленной установки.</span><span class="sxs-lookup"><span data-stu-id="74e0e-104">The installer sets the **UpdateStarted** property when changes to the system have begun for this installation, including resuming a suspended installation.</span></span>

<span data-ttu-id="74e0e-105">В инструкциях условия пользовательского интерфейса это значение используется для выбора диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="74e0e-105">UI condition statements use this value to select a dialog box.</span></span> <span data-ttu-id="74e0e-106">Если это свойство задано, пользователь получит запрос после ошибки и отменяет, следует ли выполнить восстановление или продолжить работу позже.</span><span class="sxs-lookup"><span data-stu-id="74e0e-106">If this property is set, the user is asked after an error and cancellation whether to restore or to continue later.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e0e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="74e0e-107">Requirements</span></span>



| <span data-ttu-id="74e0e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="74e0e-108">Requirement</span></span> | <span data-ttu-id="74e0e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="74e0e-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e0e-110">Версия</span><span class="sxs-lookup"><span data-stu-id="74e0e-110">Version</span></span><br/> | <span data-ttu-id="74e0e-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="74e0e-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="74e0e-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="74e0e-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="74e0e-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="74e0e-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="74e0e-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="74e0e-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74e0e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="74e0e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e0e-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="74e0e-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




