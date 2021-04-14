---
description: Метод Саурцелистклеаралл, который объект Product удаляет все источники для продукта. Можно указать тип удаляемого источника.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Метод Product. Саурцелистклеаралл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651693"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="c83e2-104">Метод Product. Саурцелистклеаралл</span><span class="sxs-lookup"><span data-stu-id="c83e2-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="c83e2-105">Метод **саурцелистклеаралл** , который объект [**Product**](product-object.md) удаляет все источники для продукта.</span><span class="sxs-lookup"><span data-stu-id="c83e2-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="c83e2-106">Можно указать тип удаляемого источника.</span><span class="sxs-lookup"><span data-stu-id="c83e2-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c83e2-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="c83e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c83e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83e2-109">*Тип*</span><span class="sxs-lookup"><span data-stu-id="c83e2-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="c83e2-110">Тип удаляемого источника: МСИСАУРЦЕТИПЕ \_ Media, мсисаурцетипе \_ Network или мсисаурцетипе \_ URL.</span><span class="sxs-lookup"><span data-stu-id="c83e2-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c83e2-111">Return value</span></span>

<span data-ttu-id="c83e2-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c83e2-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83e2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c83e2-113">Requirements</span></span>



| <span data-ttu-id="c83e2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c83e2-114">Requirement</span></span> | <span data-ttu-id="c83e2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c83e2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83e2-116">Версия</span><span class="sxs-lookup"><span data-stu-id="c83e2-116">Version</span></span><br/> | <span data-ttu-id="c83e2-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c83e2-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c83e2-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c83e2-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c83e2-119">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c83e2-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c83e2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c83e2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c83e2-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c83e2-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c83e2-122">IID</span><span class="sxs-lookup"><span data-stu-id="c83e2-122">IID</span></span><br/>     | <span data-ttu-id="c83e2-123">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c83e2-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c83e2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c83e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83e2-125">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="c83e2-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="c83e2-126">**мсисаурцелистклеарсаурце**</span><span class="sxs-lookup"><span data-stu-id="c83e2-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="c83e2-127">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="c83e2-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




