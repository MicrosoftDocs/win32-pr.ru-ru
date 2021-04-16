---
description: Возвращает объект Рекордлист, перечисляющий список продуктов.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Свойство Installer. Продуктсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651986"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="cb9f9-103">Свойство Installer. Продуктсекс</span><span class="sxs-lookup"><span data-stu-id="cb9f9-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="cb9f9-104">Свойство **продуктсекс** возвращает объект [**рекордлист**](recordlist-object.md) , перечисляющий список продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb9f9-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="cb9f9-105">Это свойство вызывает [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span><span class="sxs-lookup"><span data-stu-id="cb9f9-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="cb9f9-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cb9f9-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb9f9-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="cb9f9-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cb9f9-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9f9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cb9f9-109">Requirements</span></span>



| <span data-ttu-id="cb9f9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cb9f9-110">Requirement</span></span> | <span data-ttu-id="cb9f9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cb9f9-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9f9-112">Версия</span><span class="sxs-lookup"><span data-stu-id="cb9f9-112">Version</span></span><br/> | <span data-ttu-id="cb9f9-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb9f9-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cb9f9-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb9f9-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cb9f9-115">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb9f9-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="cb9f9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="cb9f9-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb9f9-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb9f9-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="cb9f9-118">IID</span><span class="sxs-lookup"><span data-stu-id="cb9f9-118">IID</span></span><br/>     | <span data-ttu-id="cb9f9-119">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cb9f9-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="cb9f9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb9f9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9f9-121">**Установщик**</span><span class="sxs-lookup"><span data-stu-id="cb9f9-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="cb9f9-122">**мсиенумпродуктсекс**</span><span class="sxs-lookup"><span data-stu-id="cb9f9-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="cb9f9-123">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="cb9f9-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="cb9f9-124">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="cb9f9-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




