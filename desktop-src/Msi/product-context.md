---
description: Свойство Context Возвращает контекст этого продукта.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Свойство Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652059"
---
# <a name="productcontext-property"></a><span data-ttu-id="dd3c9-103">Свойство Product. Context</span><span class="sxs-lookup"><span data-stu-id="dd3c9-103">Product.Context property</span></span>

<span data-ttu-id="dd3c9-104">Свойство **context** Возвращает контекст этого продукта.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="dd3c9-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd3c9-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="dd3c9-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd3c9-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="dd3c9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd3c9-108">Remarks</span></span>

<span data-ttu-id="dd3c9-109">Это свойство может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="dd3c9-110">Контекст</span><span class="sxs-lookup"><span data-stu-id="dd3c9-110">Context</span></span>                        | <span data-ttu-id="dd3c9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dd3c9-111">Value</span></span> | <span data-ttu-id="dd3c9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="dd3c9-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="dd3c9-113">МСИИНСТАЛЛКОНТЕКСТ \_ усерманажед</span><span class="sxs-lookup"><span data-stu-id="dd3c9-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="dd3c9-114">1</span><span class="sxs-lookup"><span data-stu-id="dd3c9-114">1</span></span>     | <span data-ttu-id="dd3c9-115">Продукты в управляемом контексте.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-115">Products under managed context.</span></span>   |
| <span data-ttu-id="dd3c9-116">\_пользователь мсиинсталлконтекст</span><span class="sxs-lookup"><span data-stu-id="dd3c9-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="dd3c9-117">2</span><span class="sxs-lookup"><span data-stu-id="dd3c9-117">2</span></span>     | <span data-ttu-id="dd3c9-118">Продукты в неуправляемом контексте.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="dd3c9-119">МСИИНСТАЛЛКОНТЕКСТ \_ компьютер</span><span class="sxs-lookup"><span data-stu-id="dd3c9-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="dd3c9-120">4</span><span class="sxs-lookup"><span data-stu-id="dd3c9-120">4</span></span>     | <span data-ttu-id="dd3c9-121">Продукты в контексте компьютера.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="dd3c9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dd3c9-122">Requirements</span></span>



| <span data-ttu-id="dd3c9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dd3c9-123">Requirement</span></span> | <span data-ttu-id="dd3c9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dd3c9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3c9-125">Версия</span><span class="sxs-lookup"><span data-stu-id="dd3c9-125">Version</span></span><br/> | <span data-ttu-id="dd3c9-126">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd3c9-127">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd3c9-128">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dd3c9-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="dd3c9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dd3c9-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd3c9-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd3c9-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="dd3c9-131">IID</span><span class="sxs-lookup"><span data-stu-id="dd3c9-131">IID</span></span><br/>     | <span data-ttu-id="dd3c9-132">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dd3c9-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="dd3c9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd3c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3c9-134">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="dd3c9-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="dd3c9-135">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="dd3c9-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




