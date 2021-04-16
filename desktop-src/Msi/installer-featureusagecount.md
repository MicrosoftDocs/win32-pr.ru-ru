---
description: Свойство Феатуреусажекаунт — это свойство, доступное только для чтения и возвращающее количество раз, когда была использована функция.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Свойство Installer. Феатуреусажекаунт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651616"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="2df9e-103">Свойство Installer. Феатуреусажекаунт</span><span class="sxs-lookup"><span data-stu-id="2df9e-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="2df9e-104">Свойство **феатуреусажекаунт** — это свойство, доступное только для чтения и возвращающее количество раз, когда была использована функция.</span><span class="sxs-lookup"><span data-stu-id="2df9e-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="2df9e-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2df9e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df9e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2df9e-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="2df9e-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2df9e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2df9e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2df9e-108">Remarks</span></span>

<span data-ttu-id="2df9e-109">Использование методов [**усефеатуре**](installer-usefeature.md), [**провидекомпонент**](installer-providecomponent.md) или [**ПРОВИДЕКУАЛИФИЕДКОМПОНЕНТ**](installer-providequalifiedcomponent.md) или их эквивалентов API для указанного компонента увеличивает это свойство.</span><span class="sxs-lookup"><span data-stu-id="2df9e-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df9e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2df9e-110">Requirements</span></span>



| <span data-ttu-id="2df9e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2df9e-111">Requirement</span></span> | <span data-ttu-id="2df9e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2df9e-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2df9e-113">Версия</span><span class="sxs-lookup"><span data-stu-id="2df9e-113">Version</span></span><br/> | <span data-ttu-id="2df9e-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2df9e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2df9e-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2df9e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2df9e-116">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="2df9e-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2df9e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2df9e-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="2df9e-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2df9e-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2df9e-119">IID</span><span class="sxs-lookup"><span data-stu-id="2df9e-119">IID</span></span><br/>     | <span data-ttu-id="2df9e-120">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2df9e-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2df9e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2df9e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df9e-122">**мсижетфеатуреусаже**</span><span class="sxs-lookup"><span data-stu-id="2df9e-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




