---
description: Установщик задает для свойства Мсирестартманажерсессионкэй значение ключа сеанса для сеанса диспетчера перезапуска.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Мсирестартманажерсессионкэй, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669043"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="bb428-103">Мсирестартманажерсессионкэй, свойство</span><span class="sxs-lookup"><span data-stu-id="bb428-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="bb428-104">Установщик задает для свойства **мсирестартманажерсессионкэй** значение ключа сеанса для сеанса [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bb428-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="bb428-105">Пользовательские действия могут использовать сеансовый ключ для приподключения к сеансу [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bb428-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb428-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb428-106">Remarks</span></span>

<span data-ttu-id="bb428-107">Установщик задает значение свойства **мсирестартманажерсессионкэй** при инициализации, а затем очищает значение во время действия [инсталлвалидате](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bb428-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="bb428-108">Пользовательские действия, которым требуется значение свойства **мсирестартманажерсессионкэй** , должны следовать перед действием инсталлвалидате в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="bb428-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb428-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bb428-109">Requirements</span></span>



| <span data-ttu-id="bb428-110">Требование</span><span class="sxs-lookup"><span data-stu-id="bb428-110">Requirement</span></span> | <span data-ttu-id="bb428-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bb428-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb428-112">Версия</span><span class="sxs-lookup"><span data-stu-id="bb428-112">Version</span></span><br/> | <span data-ttu-id="bb428-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb428-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb428-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb428-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb428-115">Сведения о минимальном пакете обновления, требуемом для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bb428-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb428-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bb428-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb428-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb428-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bb428-118">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="bb428-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
