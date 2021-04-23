---
description: Свойство Features является свойством только для чтения, которое возвращает объект Стринглист, перечисляющий набор опубликованных компонентов для указанного продукта.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Свойство Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651620"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="118ad-103">Свойство Installer. Features</span><span class="sxs-lookup"><span data-stu-id="118ad-103">Installer.Features property</span></span>

<span data-ttu-id="118ad-104">Свойство **Features** является свойством только для чтения, которое возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор опубликованных компонентов для указанного продукта.</span><span class="sxs-lookup"><span data-stu-id="118ad-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="118ad-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="118ad-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="118ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="118ad-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="118ad-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="118ad-107">Property value</span></span>

<span data-ttu-id="118ad-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="118ad-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="118ad-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="118ad-109">Remarks</span></span>

<span data-ttu-id="118ad-110">Чтобы перечислить функции, приложение выполняет перебор объекта [**стринглист**](stringlist-object.md) , используя для каждой конструкции.</span><span class="sxs-lookup"><span data-stu-id="118ad-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="118ad-111">Поскольку функции не упорядочены, каждая новая функция имеет произвольный индекс, то есть функция может возвращать функции в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="118ad-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="118ad-112">Требования</span><span class="sxs-lookup"><span data-stu-id="118ad-112">Requirements</span></span>



| <span data-ttu-id="118ad-113">Требование</span><span class="sxs-lookup"><span data-stu-id="118ad-113">Requirement</span></span> | <span data-ttu-id="118ad-114">Значение</span><span class="sxs-lookup"><span data-stu-id="118ad-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="118ad-115">Версия</span><span class="sxs-lookup"><span data-stu-id="118ad-115">Version</span></span><br/> | <span data-ttu-id="118ad-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="118ad-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="118ad-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="118ad-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="118ad-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="118ad-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="118ad-119">DLL</span><span class="sxs-lookup"><span data-stu-id="118ad-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="118ad-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="118ad-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="118ad-121">IID</span><span class="sxs-lookup"><span data-stu-id="118ad-121">IID</span></span><br/>     | <span data-ttu-id="118ad-122">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="118ad-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="118ad-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="118ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118ad-124">**мсиенумфеатурес**</span><span class="sxs-lookup"><span data-stu-id="118ad-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="118ad-125">Функции состояния системы</span><span class="sxs-lookup"><span data-stu-id="118ad-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




