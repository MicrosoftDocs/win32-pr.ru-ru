---
description: Установщик задает для свойства System64Folder полный путь к предопределенной папке System64. Для существующего свойства System64Folder задается соответствующая 32-разрядная папка.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652220"
---
# <a name="system64folder-property"></a><span data-ttu-id="9e9a1-104">System64Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="9e9a1-104">System64Folder property</span></span>

<span data-ttu-id="9e9a1-105">Установщик задает для свойства **System64Folder** полный путь к предопределенной папке System64.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="9e9a1-106">Для существующего свойства **System64Folder** задается соответствующая 32-разрядная папка.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9a1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e9a1-107">Remarks</span></span>

<span data-ttu-id="9e9a1-108">Установщик задает это свойство для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="9e9a1-109">Например, в 64-разрядной Windows значением может быть C: \\ Window \\ System32.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="9e9a1-110">Это свойство не используется в 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="9e9a1-111">Обычно эта папка является вложенной папкой папки Windows.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="9e9a1-112">Однако он находится на сервере, настроенном для совместно используемых окон.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9a1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9e9a1-113">Requirements</span></span>



| <span data-ttu-id="9e9a1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9e9a1-114">Requirement</span></span> | <span data-ttu-id="9e9a1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9e9a1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9a1-116">Версия</span><span class="sxs-lookup"><span data-stu-id="9e9a1-116">Version</span></span><br/> | <span data-ttu-id="9e9a1-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e9a1-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e9a1-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e9a1-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9e9a1-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9a1-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e9a1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9e9a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9a1-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e9a1-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




