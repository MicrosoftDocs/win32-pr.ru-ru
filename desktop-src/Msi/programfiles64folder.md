---
description: Установщик задает для свойства ProgramFiles64Folder полный путь к предопределенной папке 64-разрядных файлов программы. Для существующего свойства ProgramFilesFolder задается соответствующая 32-разрядная папка.
ms.assetid: 9301628a-3d56-4d0a-aab5-88663742daa1
title: ProgramFiles64Folder, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb8b85e0a433a3a4b51cfe23ef2de1f75dba09c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675925"
---
# <a name="programfiles64folder-property"></a><span data-ttu-id="c8c81-104">ProgramFiles64Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="c8c81-104">ProgramFiles64Folder property</span></span>

<span data-ttu-id="c8c81-105">Установщик задает для свойства **ProgramFiles64Folder** полный путь к предопределенной папке 64-разрядных файлов программы.</span><span class="sxs-lookup"><span data-stu-id="c8c81-105">The installer sets the **ProgramFiles64Folder** property to the full path of the predefined 64-bit Program Files folder.</span></span> <span data-ttu-id="c8c81-106">Для существующего свойства [**ProgramFilesFolder**](programfilesfolder.md) задается соответствующая 32-разрядная папка.</span><span class="sxs-lookup"><span data-stu-id="c8c81-106">The existing [**ProgramFilesFolder**](programfilesfolder.md) property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c81-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8c81-107">Remarks</span></span>

<span data-ttu-id="c8c81-108">Установщик задает это свойство.</span><span class="sxs-lookup"><span data-stu-id="c8c81-108">The installer sets this property.</span></span> <span data-ttu-id="c8c81-109">Например, в 64-разрядной системе Windows значением может быть «C: \\ Program Files».</span><span class="sxs-lookup"><span data-stu-id="c8c81-109">For example, on 64-bit Windows, the value may be C:\\Program Files.</span></span> <span data-ttu-id="c8c81-110">Это свойство не используется в 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c81-110">This property is not used on 32-bit Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c81-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c8c81-111">Requirements</span></span>



| <span data-ttu-id="c8c81-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c8c81-112">Requirement</span></span> | <span data-ttu-id="c8c81-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c8c81-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c81-114">Версия</span><span class="sxs-lookup"><span data-stu-id="c8c81-114">Version</span></span><br/> | <span data-ttu-id="c8c81-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8c81-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c8c81-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8c81-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c8c81-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8c81-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c8c81-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c8c81-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8c81-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c8c81-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c81-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8c81-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




