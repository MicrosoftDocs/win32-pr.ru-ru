---
description: Свойство State возвращает состояние установки данного экземпляра продукта.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Свойство Product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652081"
---
# <a name="productstate-property"></a><span data-ttu-id="c9af5-103">Свойство Product. State</span><span class="sxs-lookup"><span data-stu-id="c9af5-103">Product.State property</span></span>

<span data-ttu-id="c9af5-104">Свойство **State** возвращает состояние установки данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="c9af5-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="c9af5-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c9af5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9af5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9af5-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="c9af5-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c9af5-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c9af5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9af5-108">Remarks</span></span>

<span data-ttu-id="c9af5-109">Это свойство возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c9af5-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="c9af5-110">Состояние установки</span><span class="sxs-lookup"><span data-stu-id="c9af5-110">Installation State</span></span>       | <span data-ttu-id="c9af5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c9af5-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="c9af5-112">INSTALLSTATE \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9af5-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="c9af5-113">Экземпляр продукта, установленный локально.</span><span class="sxs-lookup"><span data-stu-id="c9af5-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="c9af5-114">INSTALLSTATE \_ объявлено</span><span class="sxs-lookup"><span data-stu-id="c9af5-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="c9af5-115">Объявленный экземпляр продукта.</span><span class="sxs-lookup"><span data-stu-id="c9af5-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="c9af5-116">INSTALLSTATE \_ неизвестный</span><span class="sxs-lookup"><span data-stu-id="c9af5-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="c9af5-117">Экземпляр продукта неизвестен.</span><span class="sxs-lookup"><span data-stu-id="c9af5-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="c9af5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c9af5-118">Requirements</span></span>



| <span data-ttu-id="c9af5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c9af5-119">Requirement</span></span> | <span data-ttu-id="c9af5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c9af5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9af5-121">Версия</span><span class="sxs-lookup"><span data-stu-id="c9af5-121">Version</span></span><br/> | <span data-ttu-id="c9af5-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9af5-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9af5-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9af5-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9af5-124">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c9af5-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c9af5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9af5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9af5-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9af5-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c9af5-127">IID</span><span class="sxs-lookup"><span data-stu-id="c9af5-127">IID</span></span><br/>     | <span data-ttu-id="c9af5-128">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c9af5-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c9af5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9af5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9af5-130">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="c9af5-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="c9af5-131">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="c9af5-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




