---
description: Метод Усефеатуре объекта Installer увеличивает счетчик использования для определенной функции и возвращает состояние установки для этой функции. Этот метод следует использовать для указания намерения приложения использовать функцию.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Метод Installer. Усефеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652158"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="b51b6-104">Метод Installer. Усефеатуре</span><span class="sxs-lookup"><span data-stu-id="b51b6-104">Installer.UseFeature method</span></span>

<span data-ttu-id="b51b6-105">Метод **усефеатуре** объекта [**Installer**](installer-object.md) увеличивает счетчик использования для определенной функции и возвращает состояние установки для этой функции.</span><span class="sxs-lookup"><span data-stu-id="b51b6-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="b51b6-106">Этот метод следует использовать для указания намерения приложения использовать функцию.</span><span class="sxs-lookup"><span data-stu-id="b51b6-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51b6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b51b6-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="b51b6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b51b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51b6-109">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="b51b6-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="b51b6-110">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="b51b6-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="b51b6-111">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="b51b6-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="b51b6-112">Определяет используемую функцию.</span><span class="sxs-lookup"><span data-stu-id="b51b6-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="b51b6-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="b51b6-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b51b6-114">Этот параметр должен быть *мсиинсталлмоденодетектион*.</span><span class="sxs-lookup"><span data-stu-id="b51b6-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51b6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b51b6-115">Return value</span></span>

<span data-ttu-id="b51b6-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b51b6-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b51b6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b51b6-117">Remarks</span></span>

<span data-ttu-id="b51b6-118">Метод **усефеатуре** следует использовать только в тех функциях, которые опубликованы.</span><span class="sxs-lookup"><span data-stu-id="b51b6-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="b51b6-119">Приложение должно определить состояние компонента, вызвав свойство [**феатурестате**](installer-featurestate.md) или [**функции**](installer-features.md) или их эквиваленты API.</span><span class="sxs-lookup"><span data-stu-id="b51b6-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51b6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b51b6-120">Requirements</span></span>



| <span data-ttu-id="b51b6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b51b6-121">Requirement</span></span> | <span data-ttu-id="b51b6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b51b6-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51b6-123">Версия</span><span class="sxs-lookup"><span data-stu-id="b51b6-123">Version</span></span><br/> | <span data-ttu-id="b51b6-124">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b51b6-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b51b6-125">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b51b6-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b51b6-126">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="b51b6-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b51b6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b51b6-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="b51b6-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b51b6-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b51b6-129">IID</span><span class="sxs-lookup"><span data-stu-id="b51b6-129">IID</span></span><br/>     | <span data-ttu-id="b51b6-130">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b51b6-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b51b6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b51b6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51b6-132">**мсиусефеатурикс**</span><span class="sxs-lookup"><span data-stu-id="b51b6-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




