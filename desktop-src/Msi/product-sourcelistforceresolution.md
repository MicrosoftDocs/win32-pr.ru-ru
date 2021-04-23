---
description: Метод Саурцелистфорцересолутион очищает свойство Ластуседсаурце.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Метод Product. Саурцелистфорцересолутион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652085"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="bb287-103">Метод Product. Саурцелистфорцересолутион</span><span class="sxs-lookup"><span data-stu-id="bb287-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="bb287-104">Метод **саурцелистфорцересолутион** очищает свойство ластуседсаурце.</span><span class="sxs-lookup"><span data-stu-id="bb287-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="bb287-105">В этом случае установщик будет выполнять поиск действительного источника продукта в исходном списке, если в следующий раз требуется источник, например, когда установщик выполняет установку или переустановку, или когда требуется путь для запуска набора компонентов из источника.</span><span class="sxs-lookup"><span data-stu-id="bb287-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="bb287-106">Этот метод вызывает [**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="bb287-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb287-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb287-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="bb287-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb287-108">Parameters</span></span>

<span data-ttu-id="bb287-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bb287-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb287-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb287-110">Return value</span></span>

<span data-ttu-id="bb287-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bb287-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb287-112">Требования</span><span class="sxs-lookup"><span data-stu-id="bb287-112">Requirements</span></span>



| <span data-ttu-id="bb287-113">Требование</span><span class="sxs-lookup"><span data-stu-id="bb287-113">Requirement</span></span> | <span data-ttu-id="bb287-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bb287-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb287-115">Версия</span><span class="sxs-lookup"><span data-stu-id="bb287-115">Version</span></span><br/> | <span data-ttu-id="bb287-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb287-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb287-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb287-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb287-118">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bb287-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="bb287-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bb287-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb287-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb287-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="bb287-121">IID</span><span class="sxs-lookup"><span data-stu-id="bb287-121">IID</span></span><br/>     | <span data-ttu-id="bb287-122">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bb287-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="bb287-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb287-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb287-124">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="bb287-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="bb287-125">**мсисаурцелистфорцересолутион**</span><span class="sxs-lookup"><span data-stu-id="bb287-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="bb287-126">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="bb287-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




