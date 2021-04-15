---
description: Установщик задает для свойства Системфолдер полный путь к системной папке.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Системфолдер, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675874"
---
# <a name="systemfolder-property"></a><span data-ttu-id="fe241-103">Системфолдер, свойство</span><span class="sxs-lookup"><span data-stu-id="fe241-103">SystemFolder property</span></span>

<span data-ttu-id="fe241-104">Установщик задает для свойства **системфолдер** полный путь к системной папке.</span><span class="sxs-lookup"><span data-stu-id="fe241-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe241-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe241-105">Remarks</span></span>

<span data-ttu-id="fe241-106">Установщик задает это свойство.</span><span class="sxs-lookup"><span data-stu-id="fe241-106">The installer sets this property.</span></span> <span data-ttu-id="fe241-107">Например, в 32-разрядной Windows значение может быть C: \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="fe241-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="fe241-108">В 64-разрядной версии Windows значением может быть C: \\ Windows \\ SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="fe241-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="fe241-109">Обычно эта папка является вложенной папкой папки Windows.</span><span class="sxs-lookup"><span data-stu-id="fe241-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="fe241-110">Однако он находится на сервере, настроенном для совместно используемых окон.</span><span class="sxs-lookup"><span data-stu-id="fe241-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="fe241-111">Эта папка является локальной, даже если она настроена для общих окон.</span><span class="sxs-lookup"><span data-stu-id="fe241-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe241-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fe241-112">Requirements</span></span>



| <span data-ttu-id="fe241-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fe241-113">Requirement</span></span> | <span data-ttu-id="fe241-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fe241-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe241-115">Версия</span><span class="sxs-lookup"><span data-stu-id="fe241-115">Version</span></span><br/> | <span data-ttu-id="fe241-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe241-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fe241-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe241-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fe241-118">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe241-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fe241-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fe241-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe241-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fe241-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe241-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe241-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




