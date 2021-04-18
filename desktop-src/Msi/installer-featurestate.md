---
description: Свойство Феатурестате только для чтения возвращает установленное состояние компонента.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Свойство Installer. Феатурестате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651617"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="738f1-103">Свойство Installer. Феатурестате</span><span class="sxs-lookup"><span data-stu-id="738f1-103">Installer.FeatureState property</span></span>

<span data-ttu-id="738f1-104">Свойство **феатурестате** только для чтения возвращает установленное состояние компонента.</span><span class="sxs-lookup"><span data-stu-id="738f1-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="738f1-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="738f1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="738f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="738f1-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="738f1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="738f1-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="738f1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="738f1-108">Remarks</span></span>

<span data-ttu-id="738f1-109">Это свойство возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="738f1-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="738f1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="738f1-110">Value</span></span>                     | <span data-ttu-id="738f1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="738f1-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="738f1-112">мсиинсталлстатеабсент</span><span class="sxs-lookup"><span data-stu-id="738f1-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="738f1-113">Компонент не установлен.</span><span class="sxs-lookup"><span data-stu-id="738f1-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="738f1-114">мсиинсталлстатеадвертисед</span><span class="sxs-lookup"><span data-stu-id="738f1-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="738f1-115">Эта функция объявлена.</span><span class="sxs-lookup"><span data-stu-id="738f1-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="738f1-116">мсиинсталлстателокал</span><span class="sxs-lookup"><span data-stu-id="738f1-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="738f1-117">Компонент устанавливается для локального запуска.</span><span class="sxs-lookup"><span data-stu-id="738f1-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="738f1-118">мсиинсталлстатесаурце</span><span class="sxs-lookup"><span data-stu-id="738f1-118">msiInstallStateSource</span></span>     | <span data-ttu-id="738f1-119">Компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="738f1-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="738f1-120">мсиинсталлстатеинвалидарг</span><span class="sxs-lookup"><span data-stu-id="738f1-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="738f1-121">Функции передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="738f1-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="738f1-122">мсиинсталлстатеункновн</span><span class="sxs-lookup"><span data-stu-id="738f1-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="738f1-123">Код продукта или компонента неизвестен.</span><span class="sxs-lookup"><span data-stu-id="738f1-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="738f1-124">мсиинсталлстатебадконфиг</span><span class="sxs-lookup"><span data-stu-id="738f1-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="738f1-125">Данные конфигурации повреждены.</span><span class="sxs-lookup"><span data-stu-id="738f1-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="738f1-126">Свойство **феатурестате** не проверяет, доступна ли функция.</span><span class="sxs-lookup"><span data-stu-id="738f1-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="738f1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="738f1-127">Requirements</span></span>



| <span data-ttu-id="738f1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="738f1-128">Requirement</span></span> | <span data-ttu-id="738f1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="738f1-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="738f1-130">Версия</span><span class="sxs-lookup"><span data-stu-id="738f1-130">Version</span></span><br/> | <span data-ttu-id="738f1-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="738f1-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="738f1-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="738f1-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="738f1-133">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="738f1-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="738f1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="738f1-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="738f1-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738f1-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="738f1-136">IID</span><span class="sxs-lookup"><span data-stu-id="738f1-136">IID</span></span><br/>     | <span data-ttu-id="738f1-137">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="738f1-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="738f1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="738f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738f1-139">**мсикуерифеатурестате**</span><span class="sxs-lookup"><span data-stu-id="738f1-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




