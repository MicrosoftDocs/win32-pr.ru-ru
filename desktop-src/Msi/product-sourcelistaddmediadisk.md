---
description: Метод Саурцелистаддмедиадиск добавляет диск к набору зарегистрированных дисков. Принимает параметры DiskID, VolumeLabel и DiskPrompt в качестве параметров. Этот метод вызывает в Мсисаурцелистаддмедиадиск.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Метод Product. Саурцелистаддмедиадиск
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651694"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="3bf89-105">Метод Product. Саурцелистаддмедиадиск</span><span class="sxs-lookup"><span data-stu-id="3bf89-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="3bf89-106">Метод **саурцелистаддмедиадиск** добавляет диск к набору зарегистрированных дисков.</span><span class="sxs-lookup"><span data-stu-id="3bf89-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="3bf89-107">Принимает параметры *DiskID*, *VolumeLabel* и *DiskPrompt* в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="3bf89-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="3bf89-108">Этот метод вызывает в [**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="3bf89-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf89-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bf89-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="3bf89-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bf89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf89-111">*DiskID*</span><span class="sxs-lookup"><span data-stu-id="3bf89-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf89-112">Этот параметр задает идентификатор добавляемого или обновляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3bf89-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="3bf89-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="3bf89-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf89-114">Этот параметр задает метку добавляемого или обновляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3bf89-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="3bf89-115">Обновление перезаписывает существующую метку тома в реестре.</span><span class="sxs-lookup"><span data-stu-id="3bf89-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="3bf89-116">Чтобы изменить только приглашение на диск, получите имеющуюся метку зарегистрированного тома и укажите ее вместе с новым диском.</span><span class="sxs-lookup"><span data-stu-id="3bf89-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="3bf89-117">Пустая строка для этого параметра регистрирует пустую строку (в длину 0 байт) в качестве метки тома.</span><span class="sxs-lookup"><span data-stu-id="3bf89-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="3bf89-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="3bf89-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf89-119">Этот параметр позволяет ввести в диск запрос на добавление или обновление диска.</span><span class="sxs-lookup"><span data-stu-id="3bf89-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="3bf89-120">Обновление перезаписывает существующий диск в реестре.</span><span class="sxs-lookup"><span data-stu-id="3bf89-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="3bf89-121">Чтобы изменить только метку тома, получите существующий дисковый запрос из реестра и укажите для него новую метку тома.</span><span class="sxs-lookup"><span data-stu-id="3bf89-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="3bf89-122">Пустая строка для этого параметра регистрирует пустую строку (в длину 0 байт) в качестве запроса диска.</span><span class="sxs-lookup"><span data-stu-id="3bf89-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf89-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bf89-123">Return value</span></span>

<span data-ttu-id="3bf89-124">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3bf89-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf89-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3bf89-125">Requirements</span></span>



| <span data-ttu-id="3bf89-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3bf89-126">Requirement</span></span> | <span data-ttu-id="3bf89-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3bf89-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf89-128">Версия</span><span class="sxs-lookup"><span data-stu-id="3bf89-128">Version</span></span><br/> | <span data-ttu-id="3bf89-129">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bf89-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bf89-130">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bf89-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bf89-131">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3bf89-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3bf89-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3bf89-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="3bf89-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bf89-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3bf89-134">IID</span><span class="sxs-lookup"><span data-stu-id="3bf89-134">IID</span></span><br/>     | <span data-ttu-id="3bf89-135">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3bf89-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="3bf89-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bf89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf89-137">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="3bf89-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="3bf89-138">**мсисаурцелистаддмедиадиск**</span><span class="sxs-lookup"><span data-stu-id="3bf89-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="3bf89-139">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="3bf89-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




