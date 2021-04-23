---
description: Метод Саурцелистклеарсаурце удаляет сеть или источник URL-адреса. Принимает тип, исходный путь и источник, в качестве параметров для удаления. Этот метод вызывает Мсисаурцелистклеарсаурце.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Метод Product. Саурцелистклеарсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651691"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="3a99e-105">Метод Product. Саурцелистклеарсаурце</span><span class="sxs-lookup"><span data-stu-id="3a99e-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="3a99e-106">Метод **саурцелистклеарсаурце** удаляет сеть или источник URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="3a99e-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="3a99e-107">Принимает *тип* *, исходный путь и источник*, в качестве параметров для удаления.</span><span class="sxs-lookup"><span data-stu-id="3a99e-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="3a99e-108">Этот метод вызывает [**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="3a99e-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a99e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a99e-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="3a99e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a99e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a99e-111">*Тип*</span><span class="sxs-lookup"><span data-stu-id="3a99e-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="3a99e-112">Тип удаляемого источника: МСИСАУРЦЕТИПЕ \_ Network или мсисаурцетипе \_ URL.</span><span class="sxs-lookup"><span data-stu-id="3a99e-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="3a99e-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="3a99e-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="3a99e-114">Путь к удаляемому источнику.</span><span class="sxs-lookup"><span data-stu-id="3a99e-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a99e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a99e-115">Return value</span></span>

<span data-ttu-id="3a99e-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a99e-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a99e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3a99e-117">Requirements</span></span>



| <span data-ttu-id="3a99e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3a99e-118">Requirement</span></span> | <span data-ttu-id="3a99e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3a99e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a99e-120">Версия</span><span class="sxs-lookup"><span data-stu-id="3a99e-120">Version</span></span><br/> | <span data-ttu-id="3a99e-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a99e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3a99e-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a99e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3a99e-123">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3a99e-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3a99e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3a99e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a99e-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a99e-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3a99e-126">IID</span><span class="sxs-lookup"><span data-stu-id="3a99e-126">IID</span></span><br/>     | <span data-ttu-id="3a99e-127">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3a99e-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="3a99e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a99e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a99e-129">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="3a99e-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="3a99e-130">**мсисаурцелистклеарсаурце**</span><span class="sxs-lookup"><span data-stu-id="3a99e-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="3a99e-131">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="3a99e-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




