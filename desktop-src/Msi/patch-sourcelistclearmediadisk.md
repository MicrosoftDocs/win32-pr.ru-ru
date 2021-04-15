---
description: Метод Саурцелистклеармедиадиск объекта Patch удаляет указанный диск из набора зарегистрированных дисков для исправления. Принимает DiskID в качестве параметра. Этот метод вызывает Мсисаурцелистклеармедиадиск.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Метод PATCH. Саурцелистклеармедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651709"
---
# <a name="patchsourcelistclearmediadisk-method"></a><span data-ttu-id="7c9be-105">Метод PATCH. Саурцелистклеармедиадиск</span><span class="sxs-lookup"><span data-stu-id="7c9be-105">Patch.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="7c9be-106">Метод **саурцелистклеармедиадиск** объекта [**Patch**](patch-object.md) удаляет указанный диск из набора зарегистрированных дисков для исправления.</span><span class="sxs-lookup"><span data-stu-id="7c9be-106">The **SourceListClearMediaDisk** method of the [**Patch**](patch-object.md) object removes a specified disk from the set of registered disks for a patch.</span></span> <span data-ttu-id="7c9be-107">Принимает *DiskID* в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="7c9be-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="7c9be-108">Этот метод вызывает [**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="7c9be-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9be-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c9be-109">Syntax</span></span>


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="7c9be-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c9be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9be-111">*DiskID*</span><span class="sxs-lookup"><span data-stu-id="7c9be-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="7c9be-112">Этот параметр задает идентификатор удаляемого диска.</span><span class="sxs-lookup"><span data-stu-id="7c9be-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9be-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c9be-113">Return value</span></span>

<span data-ttu-id="7c9be-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7c9be-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9be-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7c9be-115">Requirements</span></span>



| <span data-ttu-id="7c9be-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7c9be-116">Requirement</span></span> | <span data-ttu-id="7c9be-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7c9be-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9be-118">Версия</span><span class="sxs-lookup"><span data-stu-id="7c9be-118">Version</span></span><br/> | <span data-ttu-id="7c9be-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c9be-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c9be-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c9be-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c9be-121">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7c9be-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="7c9be-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7c9be-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c9be-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c9be-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="7c9be-124">IID</span><span class="sxs-lookup"><span data-stu-id="7c9be-124">IID</span></span><br/>     | <span data-ttu-id="7c9be-125">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c9be-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="7c9be-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c9be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9be-127">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="7c9be-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="7c9be-128">**мсисаурцелистклеармедиадиск**</span><span class="sxs-lookup"><span data-stu-id="7c9be-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="7c9be-129">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="7c9be-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




