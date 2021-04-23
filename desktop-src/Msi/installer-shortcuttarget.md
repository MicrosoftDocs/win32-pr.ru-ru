---
description: Свойство Шорткуттаржет объекта installer проверяет ярлык и возвращает его продукт, имя функции и компонент, если он доступен.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Свойство Installer. Шорткуттаржет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652159"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="cb0e3-103">Свойство Installer. Шорткуттаржет</span><span class="sxs-lookup"><span data-stu-id="cb0e3-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="cb0e3-104">Свойство **шорткуттаржет** объекта [**Installer**](installer-object.md) проверяет ярлык и возвращает его продукт, имя функции и компонент, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="cb0e3-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb0e3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb0e3-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="cb0e3-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cb0e3-107">Property value</span></span>

<span data-ttu-id="cb0e3-108">Полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb0e3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb0e3-109">Remarks</span></span>

<span data-ttu-id="cb0e3-110">Шорткуттаржет возвращает [**объект Record**](record-object.md) , содержащий три поля:</span><span class="sxs-lookup"><span data-stu-id="cb0e3-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="cb0e3-111">Поле 1 — это идентификатор GUID для кода продукта ярлыка, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="cb0e3-112">Это поле может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-112">This field can be null.</span></span>
-   <span data-ttu-id="cb0e3-113">Поле 2 — это идентификатор компонента ярлыка, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="cb0e3-114">Это поле может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-114">This field can be null.</span></span>
-   <span data-ttu-id="cb0e3-115">Поле 3 — это идентификатор GUID для кода компонента, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="cb0e3-116">Это поле может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb0e3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cb0e3-117">Requirements</span></span>



| <span data-ttu-id="cb0e3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cb0e3-118">Requirement</span></span> | <span data-ttu-id="cb0e3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cb0e3-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0e3-120">Версия</span><span class="sxs-lookup"><span data-stu-id="cb0e3-120">Version</span></span><br/> | <span data-ttu-id="cb0e3-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cb0e3-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb0e3-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cb0e3-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb0e3-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cb0e3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb0e3-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb0e3-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb0e3-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cb0e3-126">IID</span><span class="sxs-lookup"><span data-stu-id="cb0e3-126">IID</span></span><br/>     | <span data-ttu-id="cb0e3-127">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cb0e3-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="cb0e3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb0e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0e3-129">**мсижетфеатурестате**</span><span class="sxs-lookup"><span data-stu-id="cb0e3-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="cb0e3-130">**мсижеткомпонентстате**</span><span class="sxs-lookup"><span data-stu-id="cb0e3-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




