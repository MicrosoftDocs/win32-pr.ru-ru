---
description: Свойство Патчесекс возвращает объект Рекордлист, перечисляющий список исправлений.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Свойство Installer. Патчесекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651659"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="be84d-103">Свойство Installer. Патчесекс</span><span class="sxs-lookup"><span data-stu-id="be84d-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="be84d-104">Свойство **патчесекс** возвращает объект [**рекордлист**](recordlist-object.md) , перечисляющий список исправлений.</span><span class="sxs-lookup"><span data-stu-id="be84d-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="be84d-105">Это свойство вызывает [**мсиенумпатчесекс**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="be84d-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="be84d-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be84d-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be84d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be84d-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="be84d-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="be84d-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="be84d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="be84d-109">Requirements</span></span>



| <span data-ttu-id="be84d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="be84d-110">Requirement</span></span> | <span data-ttu-id="be84d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="be84d-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be84d-112">Версия</span><span class="sxs-lookup"><span data-stu-id="be84d-112">Version</span></span><br/> | <span data-ttu-id="be84d-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be84d-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be84d-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be84d-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be84d-115">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="be84d-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="be84d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="be84d-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="be84d-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be84d-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="be84d-118">IID</span><span class="sxs-lookup"><span data-stu-id="be84d-118">IID</span></span><br/>     | <span data-ttu-id="be84d-119">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be84d-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="be84d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be84d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be84d-121">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="be84d-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="be84d-122">**мсиенумпатчесекс**</span><span class="sxs-lookup"><span data-stu-id="be84d-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="be84d-123">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="be84d-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="be84d-124">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="be84d-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




