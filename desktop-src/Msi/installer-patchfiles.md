---
description: Свойство Патчфилес возвращает объект Стринглист, содержащий список файлов, которые можно обновить с помощью предоставленного списка исправлений.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Свойство Installer. Патчфилес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652237"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="1e729-103">Свойство Installer. Патчфилес</span><span class="sxs-lookup"><span data-stu-id="1e729-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="1e729-104">Свойство **патчфилес** возвращает объект [**стринглист**](stringlist-object.md) , содержащий список файлов, которые можно обновить с помощью предоставленного списка исправлений.</span><span class="sxs-lookup"><span data-stu-id="1e729-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="1e729-105">Это свойство вызывает [**мсижетпатчфилелист**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="1e729-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="1e729-106">Дополнительные сведения об использовании свойства **патчфилес** см. [в разделе Список файлов, которые можно обновить](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="1e729-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="1e729-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e729-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e729-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e729-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="1e729-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e729-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="1e729-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1e729-110">Requirements</span></span>



| <span data-ttu-id="1e729-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1e729-111">Requirement</span></span> | <span data-ttu-id="1e729-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1e729-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e729-113">Версия</span><span class="sxs-lookup"><span data-stu-id="1e729-113">Version</span></span><br/> | <span data-ttu-id="1e729-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e729-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1e729-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e729-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1e729-116">Установщик Windows 4,5 в Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e729-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="1e729-117">DLL</span><span class="sxs-lookup"><span data-stu-id="1e729-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e729-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e729-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="1e729-119">IID</span><span class="sxs-lookup"><span data-stu-id="1e729-119">IID</span></span><br/>     | <span data-ttu-id="1e729-120">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1e729-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="1e729-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e729-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e729-122">**Объект установщика**</span><span class="sxs-lookup"><span data-stu-id="1e729-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="1e729-123">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="1e729-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




