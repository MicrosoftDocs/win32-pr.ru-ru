---
description: Свойство Медиадискс перечисляет все диски носителя для данного экземпляра продукта. Это свойство вызывает Мсисаурцелистенуммедиадискс. Возвращает сведения о диске в виде массива объектов записи.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Свойство patch. Медиадискс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651636"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="82711-105">Свойство patch. Медиадискс</span><span class="sxs-lookup"><span data-stu-id="82711-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="82711-106">Свойство **медиадискс** перечисляет все диски носителя для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="82711-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="82711-107">Это свойство вызывает [**мсисаурцелистенуммедиадискс**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="82711-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="82711-108">Возвращает сведения о диске в виде массива объектов [**записи**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="82711-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="82711-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82711-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82711-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82711-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="82711-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="82711-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="82711-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82711-112">Remarks</span></span>

<span data-ttu-id="82711-113">В каждой записи первое поле содержит идентификатор диска, второе поле содержит метку тома, а третье поле содержит запрос диска, зарегистрированный для диска.</span><span class="sxs-lookup"><span data-stu-id="82711-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="82711-114">Требования</span><span class="sxs-lookup"><span data-stu-id="82711-114">Requirements</span></span>



| <span data-ttu-id="82711-115">Требование</span><span class="sxs-lookup"><span data-stu-id="82711-115">Requirement</span></span> | <span data-ttu-id="82711-116">Значение</span><span class="sxs-lookup"><span data-stu-id="82711-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82711-117">Версия</span><span class="sxs-lookup"><span data-stu-id="82711-117">Version</span></span><br/> | <span data-ttu-id="82711-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82711-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82711-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82711-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82711-120">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="82711-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="82711-121">DLL</span><span class="sxs-lookup"><span data-stu-id="82711-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="82711-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82711-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="82711-123">IID</span><span class="sxs-lookup"><span data-stu-id="82711-123">IID</span></span><br/>     | <span data-ttu-id="82711-124">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82711-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="82711-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82711-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82711-126">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="82711-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="82711-127">**мсисаурцелистенуммедиадискс**</span><span class="sxs-lookup"><span data-stu-id="82711-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="82711-128">**Записать**</span><span class="sxs-lookup"><span data-stu-id="82711-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="82711-129">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="82711-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




