---
description: Свойство Products является свойством только для чтения, которое возвращает набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Свойство Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651911"
---
# <a name="installerproducts-property"></a><span data-ttu-id="50f11-103">Свойство Installer. Products</span><span class="sxs-lookup"><span data-stu-id="50f11-103">Installer.Products property</span></span>

<span data-ttu-id="50f11-104">Свойство **Products** является свойством только для чтения, которое возвращает [](stringlist-object.md) набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера.</span><span class="sxs-lookup"><span data-stu-id="50f11-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="50f11-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="50f11-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f11-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50f11-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="50f11-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="50f11-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="50f11-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50f11-108">Remarks</span></span>

<span data-ttu-id="50f11-109">Чтобы перечислить продукты, приложение выполняет итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="50f11-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="50f11-110">Поскольку продукты не упорядочены, у каждого нового продукта есть произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="50f11-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="50f11-111">Это означает, что функция может возвращать продукты в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="50f11-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="50f11-112">Требования</span><span class="sxs-lookup"><span data-stu-id="50f11-112">Requirements</span></span>



| <span data-ttu-id="50f11-113">Требование</span><span class="sxs-lookup"><span data-stu-id="50f11-113">Requirement</span></span> | <span data-ttu-id="50f11-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50f11-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f11-115">Версия</span><span class="sxs-lookup"><span data-stu-id="50f11-115">Version</span></span><br/> | <span data-ttu-id="50f11-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50f11-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50f11-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="50f11-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50f11-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="50f11-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="50f11-119">DLL</span><span class="sxs-lookup"><span data-stu-id="50f11-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="50f11-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f11-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="50f11-121">IID</span><span class="sxs-lookup"><span data-stu-id="50f11-121">IID</span></span><br/>     | <span data-ttu-id="50f11-122">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="50f11-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="50f11-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50f11-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f11-124">**мсиенумпродуктс**</span><span class="sxs-lookup"><span data-stu-id="50f11-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




