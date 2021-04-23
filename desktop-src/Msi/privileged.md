---
description: Свойство Privileges указывает, выполняется ли установка в контексте повышенных привилегий.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Привилегированное свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652205"
---
# <a name="privileged-property"></a><span data-ttu-id="34e74-103">Привилегированное свойство</span><span class="sxs-lookup"><span data-stu-id="34e74-103">Privileged property</span></span>

<span data-ttu-id="34e74-104">Свойство **Privileges** указывает, выполняется ли установка в контексте повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="34e74-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="34e74-105">Установщик задает это свойство, если пользователь имеет права администратора, если приложение назначено системным администратором или если для политики пользователя и компьютера AlwaysInstallElevated задано значение true.</span><span class="sxs-lookup"><span data-stu-id="34e74-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="34e74-106">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="34e74-106">Default Value</span></span>

<span data-ttu-id="34e74-107">Установщик не устанавливает это свойство, если пользователю не разрешено устанавливать с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="34e74-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e74-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34e74-108">Remarks</span></span>

<span data-ttu-id="34e74-109">Разработчики пакетов установщика могут использовать **привилегированное** свойство, чтобы установить условную установку на основе системной политики, пользователя, который является администратором, или назначить администратором.</span><span class="sxs-lookup"><span data-stu-id="34e74-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="34e74-110">При работе в Windows Vista **привилегированные** и [**AdminUser**](adminuser.md) совпадают.</span><span class="sxs-lookup"><span data-stu-id="34e74-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e74-111">Требования</span><span class="sxs-lookup"><span data-stu-id="34e74-111">Requirements</span></span>



| <span data-ttu-id="34e74-112">Требование</span><span class="sxs-lookup"><span data-stu-id="34e74-112">Requirement</span></span> | <span data-ttu-id="34e74-113">Значение</span><span class="sxs-lookup"><span data-stu-id="34e74-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e74-114">Версия</span><span class="sxs-lookup"><span data-stu-id="34e74-114">Version</span></span><br/> | <span data-ttu-id="34e74-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34e74-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34e74-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34e74-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34e74-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34e74-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="34e74-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="34e74-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34e74-119">См. также</span><span class="sxs-lookup"><span data-stu-id="34e74-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e74-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="34e74-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




