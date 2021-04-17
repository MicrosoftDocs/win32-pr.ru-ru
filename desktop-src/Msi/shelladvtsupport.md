---
description: Свойство Шелладвтсуппорт задается программой установки, если интерфейс Ишелллинк системы поддерживает разрешение дескриптора установщика.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Шелладвтсуппорт, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674847"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="705cc-103">Шелладвтсуппорт, свойство</span><span class="sxs-lookup"><span data-stu-id="705cc-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="705cc-104">Свойство **шелладвтсуппорт** задается программой установки, если интерфейс [**ишелллинк**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) системы поддерживает разрешение дескриптора установщика.</span><span class="sxs-lookup"><span data-stu-id="705cc-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="705cc-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="705cc-105">Remarks</span></span>

<span data-ttu-id="705cc-106">Если это свойство задано, интерфейс [**ишелллинк**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) системы поддерживает разрешение дескрипторов установщика.</span><span class="sxs-lookup"><span data-stu-id="705cc-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="705cc-107">Это поддерживается в Windows 2000 и системах с Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="705cc-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="705cc-108">Если это свойство не задано, установщик имеет поведение по умолчанию для создания необъявленных компонентов во время установки (локально или из источника).</span><span class="sxs-lookup"><span data-stu-id="705cc-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="705cc-109">Требования</span><span class="sxs-lookup"><span data-stu-id="705cc-109">Requirements</span></span>



| <span data-ttu-id="705cc-110">Требование</span><span class="sxs-lookup"><span data-stu-id="705cc-110">Requirement</span></span> | <span data-ttu-id="705cc-111">Значение</span><span class="sxs-lookup"><span data-stu-id="705cc-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705cc-112">Версия</span><span class="sxs-lookup"><span data-stu-id="705cc-112">Version</span></span><br/> | <span data-ttu-id="705cc-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="705cc-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="705cc-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="705cc-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="705cc-115">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="705cc-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="705cc-116">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="705cc-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="705cc-117">См. также</span><span class="sxs-lookup"><span data-stu-id="705cc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="705cc-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="705cc-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="705cc-119">Поддержка платформ объявления</span><span class="sxs-lookup"><span data-stu-id="705cc-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
