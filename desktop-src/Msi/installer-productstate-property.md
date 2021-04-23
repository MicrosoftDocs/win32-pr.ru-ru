---
description: Свойство Продуктстате является свойством только для чтения, которое возвращает сведения о состоянии установки для продукта.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Метод свойства Installer. Продуктстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651985"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="ca6ee-103">Метод свойства Installer. Продуктстате</span><span class="sxs-lookup"><span data-stu-id="ca6ee-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="ca6ee-104">**Свойство продуктстате** является свойством только для чтения, которое возвращает сведения о состоянии установки для продукта.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca6ee-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="ca6ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca6ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca6ee-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="ca6ee-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6ee-108">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca6ee-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca6ee-109">Return value</span></span>

<span data-ttu-id="ca6ee-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca6ee-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca6ee-111">Remarks</span></span>

<span data-ttu-id="ca6ee-112">Возвращает одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="ca6ee-113">Состояние установки</span><span class="sxs-lookup"><span data-stu-id="ca6ee-113">Installation state</span></span>        | <span data-ttu-id="ca6ee-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ca6ee-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="ca6ee-115">мсиинсталлстатеабсент</span><span class="sxs-lookup"><span data-stu-id="ca6ee-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="ca6ee-116">Продукт устанавливается для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="ca6ee-117">мсиинсталлстатедефаулт</span><span class="sxs-lookup"><span data-stu-id="ca6ee-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="ca6ee-118">Продукт установлен для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="ca6ee-119">мсиинсталлстатеадвертисед</span><span class="sxs-lookup"><span data-stu-id="ca6ee-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="ca6ee-120">Продукт объявлен, но не установлен.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="ca6ee-121">мсиинсталлстатеинвалидарг</span><span class="sxs-lookup"><span data-stu-id="ca6ee-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="ca6ee-122">Функции передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="ca6ee-123">мсиинсталлстатеункновн</span><span class="sxs-lookup"><span data-stu-id="ca6ee-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="ca6ee-124">Продукт не объявлен и не установлен.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="ca6ee-125">мсиинсталлстатебадконфиг</span><span class="sxs-lookup"><span data-stu-id="ca6ee-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="ca6ee-126">Данные конфигурации повреждены.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="ca6ee-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ca6ee-127">Requirements</span></span>



| <span data-ttu-id="ca6ee-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ca6ee-128">Requirement</span></span> | <span data-ttu-id="ca6ee-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ca6ee-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6ee-130">Версия</span><span class="sxs-lookup"><span data-stu-id="ca6ee-130">Version</span></span><br/> | <span data-ttu-id="ca6ee-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca6ee-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca6ee-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca6ee-133">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca6ee-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ca6ee-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ca6ee-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca6ee-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca6ee-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ca6ee-136">IID</span><span class="sxs-lookup"><span data-stu-id="ca6ee-136">IID</span></span><br/>     | <span data-ttu-id="ca6ee-137">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ca6ee-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="ca6ee-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca6ee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6ee-139">**мсикуерипродуктстате**</span><span class="sxs-lookup"><span data-stu-id="ca6ee-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




