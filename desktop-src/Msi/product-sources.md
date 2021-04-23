---
description: Свойство Sources перечисляет все источники для экземпляра продукта.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Свойство Product. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675976"
---
# <a name="productsources-property"></a><span data-ttu-id="563fe-103">Свойство Product. sources</span><span class="sxs-lookup"><span data-stu-id="563fe-103">Product.Sources property</span></span>

<span data-ttu-id="563fe-104">Свойство **Sources** перечисляет все источники для экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="563fe-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="563fe-105">Это свойство вызывает [**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) и возвращает массив строк и принимает тип источника в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="563fe-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="563fe-106">Исходный тип может быть МСИСАУРЦЕТИПЕ \_ сетевым или мсисаурцетипе \_ URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="563fe-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="563fe-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="563fe-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="563fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="563fe-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="563fe-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="563fe-109">Property value</span></span>

<span data-ttu-id="563fe-110">Тип источника для перечисления.</span><span class="sxs-lookup"><span data-stu-id="563fe-110">The type of source to enumerate.</span></span> <span data-ttu-id="563fe-111">Значение может быть *мсиинсталлсаурцетипенетворк* (1) или *мсиинсталлсаурцетипеурл* (2).</span><span class="sxs-lookup"><span data-stu-id="563fe-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="563fe-112">Требования</span><span class="sxs-lookup"><span data-stu-id="563fe-112">Requirements</span></span>



| <span data-ttu-id="563fe-113">Требование</span><span class="sxs-lookup"><span data-stu-id="563fe-113">Requirement</span></span> | <span data-ttu-id="563fe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="563fe-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563fe-115">Версия</span><span class="sxs-lookup"><span data-stu-id="563fe-115">Version</span></span><br/> | <span data-ttu-id="563fe-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="563fe-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="563fe-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="563fe-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="563fe-118">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="563fe-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="563fe-119">DLL</span><span class="sxs-lookup"><span data-stu-id="563fe-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="563fe-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="563fe-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="563fe-121">IID</span><span class="sxs-lookup"><span data-stu-id="563fe-121">IID</span></span><br/>     | <span data-ttu-id="563fe-122">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="563fe-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="563fe-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="563fe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563fe-124">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="563fe-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="563fe-125">**мсисаурцелистенумсаурцес**</span><span class="sxs-lookup"><span data-stu-id="563fe-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="563fe-126">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="563fe-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




