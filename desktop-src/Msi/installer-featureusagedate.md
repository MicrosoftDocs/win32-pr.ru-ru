---
description: Свойство Феатуреусажедате является свойством только для чтения, которое возвращает дату последнего использования указанного компонента.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Свойство Installer. Феатуреусажедате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651612"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="f1e34-103">Свойство Installer. Феатуреусажедате</span><span class="sxs-lookup"><span data-stu-id="f1e34-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="f1e34-104">Свойство **феатуреусажедате** является свойством только для чтения, которое возвращает дату последнего использования указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="f1e34-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="f1e34-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f1e34-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e34-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1e34-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="f1e34-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f1e34-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e34-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1e34-108">Remarks</span></span>

<span data-ttu-id="f1e34-109">Это свойство задается с помощью методов [**усефеатуре**](installer-usefeature.md), [**провидекомпонент**](installer-providecomponent.md) или [**ПРОВИДЕКУАЛИФИЕДКОМПОНЕНТ**](installer-providequalifiedcomponent.md) или их эквивалентов API для указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="f1e34-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="f1e34-110">Дата указывается в формате даты MS-DOS, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f1e34-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="f1e34-111">Bits</span><span class="sxs-lookup"><span data-stu-id="f1e34-111">Bits</span></span> | <span data-ttu-id="f1e34-112">Содержимое</span><span class="sxs-lookup"><span data-stu-id="f1e34-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="f1e34-113">0-4</span><span class="sxs-lookup"><span data-stu-id="f1e34-113">0-4</span></span>  | <span data-ttu-id="f1e34-114">День месяца (1-31)</span><span class="sxs-lookup"><span data-stu-id="f1e34-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="f1e34-115">5-8</span><span class="sxs-lookup"><span data-stu-id="f1e34-115">5-8</span></span>  | <span data-ttu-id="f1e34-116">Месяц (1 = Январь, 2 = Февраль и т. д.)</span><span class="sxs-lookup"><span data-stu-id="f1e34-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="f1e34-117">9-15</span><span class="sxs-lookup"><span data-stu-id="f1e34-117">9-15</span></span> | <span data-ttu-id="f1e34-118">Смещение года от 1980 (Добавление 1980 для получения фактического года)</span><span class="sxs-lookup"><span data-stu-id="f1e34-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f1e34-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f1e34-119">Requirements</span></span>



| <span data-ttu-id="f1e34-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f1e34-120">Requirement</span></span> | <span data-ttu-id="f1e34-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f1e34-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e34-122">Версия</span><span class="sxs-lookup"><span data-stu-id="f1e34-122">Version</span></span><br/> | <span data-ttu-id="f1e34-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f1e34-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f1e34-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f1e34-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f1e34-125">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1e34-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f1e34-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f1e34-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1e34-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1e34-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f1e34-128">IID</span><span class="sxs-lookup"><span data-stu-id="f1e34-128">IID</span></span><br/>     | <span data-ttu-id="f1e34-129">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f1e34-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f1e34-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1e34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e34-131">**мсижетфеатуреусаже**</span><span class="sxs-lookup"><span data-stu-id="f1e34-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




