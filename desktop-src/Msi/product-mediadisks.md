---
description: Свойство Медиадискс перечисляет все диски носителя для данного экземпляра продукта. Это свойство вызывает Мсисаурцелистенуммедиадискс. Возвращает сведения о диске в виде массива объектов Record.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Свойство Product. Медиадискс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651696"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="5e988-105">Свойство Product. Медиадискс</span><span class="sxs-lookup"><span data-stu-id="5e988-105">Product.MediaDisks property</span></span>

<span data-ttu-id="5e988-106">Свойство **медиадискс** перечисляет все диски носителя для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="5e988-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="5e988-107">Это свойство вызывает [**мсисаурцелистенуммедиадискс**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="5e988-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="5e988-108">Возвращает сведения о диске в виде массива объектов [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5e988-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="5e988-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5e988-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e988-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e988-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="5e988-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5e988-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5e988-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e988-112">Remarks</span></span>

<span data-ttu-id="5e988-113">В каждой записи первое поле содержит идентификатор диска, второе поле содержит метку тома, а третье поле содержит приглашение диска, зарегистрированное для диска.</span><span class="sxs-lookup"><span data-stu-id="5e988-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e988-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5e988-114">Requirements</span></span>



| <span data-ttu-id="5e988-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5e988-115">Requirement</span></span> | <span data-ttu-id="5e988-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5e988-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e988-117">Версия</span><span class="sxs-lookup"><span data-stu-id="5e988-117">Version</span></span><br/> | <span data-ttu-id="5e988-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e988-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5e988-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e988-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5e988-120">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5e988-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5e988-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5e988-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e988-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e988-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5e988-123">IID</span><span class="sxs-lookup"><span data-stu-id="5e988-123">IID</span></span><br/>     | <span data-ttu-id="5e988-124">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5e988-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="5e988-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e988-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e988-126">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="5e988-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="5e988-127">**мсисаурцелистенуммедиадискс**</span><span class="sxs-lookup"><span data-stu-id="5e988-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="5e988-128">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="5e988-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




