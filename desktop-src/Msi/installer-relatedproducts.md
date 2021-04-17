---
description: Свойство Релатедпродуктс только для чтения возвращает объект Стринглист, перечисляющий набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера с указанным свойством UpgradeCode в своей таблице свойств.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Свойство Installer. Релатедпродуктс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652160"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="3d08a-103">Свойство Installer. Релатедпродуктс</span><span class="sxs-lookup"><span data-stu-id="3d08a-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="3d08a-104">Свойство **релатедпродуктс** только для чтения возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор всех продуктов, установленных или объявленных для текущего пользователя и компьютера с указанным свойством [**UpgradeCode**](upgradecode.md) в своей [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d08a-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="3d08a-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3d08a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d08a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d08a-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="3d08a-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3d08a-107">Property value</span></span>

<span data-ttu-id="3d08a-108">Код обновления связанных продуктов, перечисленный установщиком.</span><span class="sxs-lookup"><span data-stu-id="3d08a-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d08a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d08a-109">Remarks</span></span>

<span data-ttu-id="3d08a-110">Чтобы перечислить связанные продукты, приложение выполняет итерацию по [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="3d08a-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="3d08a-111">Так как связанные продукты не упорядочены, любой новый связанный продукт имеет произвольный индекс.</span><span class="sxs-lookup"><span data-stu-id="3d08a-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="3d08a-112">Это означает, что функция может возвращать связанные продукты в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="3d08a-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d08a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3d08a-113">Requirements</span></span>



| <span data-ttu-id="3d08a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3d08a-114">Requirement</span></span> | <span data-ttu-id="3d08a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3d08a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d08a-116">Версия</span><span class="sxs-lookup"><span data-stu-id="3d08a-116">Version</span></span><br/> | <span data-ttu-id="3d08a-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d08a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3d08a-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3d08a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3d08a-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d08a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3d08a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3d08a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d08a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d08a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3d08a-122">IID</span><span class="sxs-lookup"><span data-stu-id="3d08a-122">IID</span></span><br/>     | <span data-ttu-id="3d08a-123">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3d08a-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3d08a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d08a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d08a-125">**мсиенумрелатедпродуктс**</span><span class="sxs-lookup"><span data-stu-id="3d08a-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




