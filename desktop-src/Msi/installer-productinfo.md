---
description: Свойство ProductInfo является свойством только для чтения, которое возвращает значение указанного атрибута для установленного или опубликованного продукта.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Свойство Installer. ProductInfo (Оемупжекс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652226"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="f9467-103">Свойство Installer. ProductInfo</span><span class="sxs-lookup"><span data-stu-id="f9467-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="f9467-104">Свойство **ProductInfo** является свойством только для чтения, которое возвращает значение указанного атрибута для установленного или опубликованного продукта.</span><span class="sxs-lookup"><span data-stu-id="f9467-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="f9467-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f9467-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9467-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9467-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="f9467-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f9467-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f9467-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9467-108">Remarks</span></span>

<span data-ttu-id="f9467-109">Свойство **ProductInfo** ("локалпаккаже") не обязательно возвращает путь к кэшированному пакету.</span><span class="sxs-lookup"><span data-stu-id="f9467-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="f9467-110">Установка режима обслуживания не должна вызываться из Локалпаккаже.</span><span class="sxs-lookup"><span data-stu-id="f9467-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="f9467-111">Кэшированный пакет предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="f9467-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9467-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f9467-112">Requirements</span></span>



| <span data-ttu-id="f9467-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f9467-113">Requirement</span></span> | <span data-ttu-id="f9467-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f9467-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9467-115">Версия</span><span class="sxs-lookup"><span data-stu-id="f9467-115">Version</span></span><br/> | <span data-ttu-id="f9467-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9467-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f9467-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9467-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f9467-118">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9467-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="f9467-119">Header</span><span class="sxs-lookup"><span data-stu-id="f9467-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f9467-120"><dt>Оемупжекс. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9467-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="f9467-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f9467-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9467-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9467-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="f9467-123">IID</span><span class="sxs-lookup"><span data-stu-id="f9467-123">IID</span></span><br/>     | <span data-ttu-id="f9467-124">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f9467-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="f9467-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9467-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9467-126">**мсижетпродуктинфо**</span><span class="sxs-lookup"><span data-stu-id="f9467-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="f9467-127">**мсижетусеринфо**</span><span class="sxs-lookup"><span data-stu-id="f9467-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="f9467-128">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="f9467-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




