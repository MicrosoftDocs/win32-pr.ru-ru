---
description: Свойство Феатурестате — это состояние установки компонента для экземпляра этого продукта. Это свойство вызывает Мсикуерифеатурестатикс с ProductCode, а также контекстом объекта. Идентификатор функции указывается в качестве параметра.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Метод Product. Феатурестате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651809"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="01a44-104">Метод Product. Феатурестате</span><span class="sxs-lookup"><span data-stu-id="01a44-104">Product.FeatureState method</span></span>

<span data-ttu-id="01a44-105">Свойство **феатурестате** — это состояние установки компонента для экземпляра этого продукта.</span><span class="sxs-lookup"><span data-stu-id="01a44-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="01a44-106">Это свойство вызывает [**мсикуерифеатурестатикс**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)с *ProductCode* *, а также* *контекстом* объекта.</span><span class="sxs-lookup"><span data-stu-id="01a44-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="01a44-107">Идентификатор функции указывается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="01a44-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a44-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01a44-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="01a44-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01a44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a44-110">*феатуреид*</span><span class="sxs-lookup"><span data-stu-id="01a44-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="01a44-111">Идентификатор компонента отображается в столбце "компонент" [таблицы функций](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="01a44-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a44-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01a44-112">Return value</span></span>

<span data-ttu-id="01a44-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01a44-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a44-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01a44-114">Remarks</span></span>

<span data-ttu-id="01a44-115">Если вызов будет выполнен, свойство будет содержать значение **типа DWORD**.</span><span class="sxs-lookup"><span data-stu-id="01a44-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="01a44-116">Состояние</span><span class="sxs-lookup"><span data-stu-id="01a44-116">State</span></span>                    | <span data-ttu-id="01a44-117">Значение</span><span class="sxs-lookup"><span data-stu-id="01a44-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="01a44-118">INSTALLSTATE \_ объявлено</span><span class="sxs-lookup"><span data-stu-id="01a44-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="01a44-119">Эта функция объявлена.</span><span class="sxs-lookup"><span data-stu-id="01a44-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="01a44-120">INSTALLSTATE \_ локальный</span><span class="sxs-lookup"><span data-stu-id="01a44-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="01a44-121">Этот компонент устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="01a44-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="01a44-122">\_источник InstallState</span><span class="sxs-lookup"><span data-stu-id="01a44-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="01a44-123">Компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="01a44-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="01a44-124">Если вызов завершается неудачей, свойство содержит код ошибки из [**мсикуерифеатурестатикс**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="01a44-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="01a44-125">Ошибка</span><span class="sxs-lookup"><span data-stu-id="01a44-125">Error</span></span>                     | <span data-ttu-id="01a44-126">Значение</span><span class="sxs-lookup"><span data-stu-id="01a44-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a44-127">Ошибка \_ отказа в доступе \_</span><span class="sxs-lookup"><span data-stu-id="01a44-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="01a44-128">Вызывающий процесс должен иметь права администратора для получения сведений о продукте, установленном для пользователя, отличного от текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="01a44-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="01a44-129">Ошибка \_ неправильной \_ конфигурации</span><span class="sxs-lookup"><span data-stu-id="01a44-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="01a44-130">Данные конфигурации повреждены.</span><span class="sxs-lookup"><span data-stu-id="01a44-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="01a44-131">Ошибка \_ недопустимого \_ параметра</span><span class="sxs-lookup"><span data-stu-id="01a44-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="01a44-132">Функции передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="01a44-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="01a44-133">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="01a44-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="01a44-134">Функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="01a44-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="01a44-135">Ошибка \_ неизвестного \_ компонента</span><span class="sxs-lookup"><span data-stu-id="01a44-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="01a44-136">Идентификатор функции не определяет известную функцию.</span><span class="sxs-lookup"><span data-stu-id="01a44-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="01a44-137">Ошибка \_ неизвестного \_ продукта</span><span class="sxs-lookup"><span data-stu-id="01a44-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="01a44-138">Код продукта не определяет известный продукт.</span><span class="sxs-lookup"><span data-stu-id="01a44-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="01a44-139">Ошибка \_ \_ при выполнении функции</span><span class="sxs-lookup"><span data-stu-id="01a44-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="01a44-140">Непредвиденный внутренний сбой.</span><span class="sxs-lookup"><span data-stu-id="01a44-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="01a44-141">Требования</span><span class="sxs-lookup"><span data-stu-id="01a44-141">Requirements</span></span>



| <span data-ttu-id="01a44-142">Требование</span><span class="sxs-lookup"><span data-stu-id="01a44-142">Requirement</span></span> | <span data-ttu-id="01a44-143">Значение</span><span class="sxs-lookup"><span data-stu-id="01a44-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a44-144">Версия</span><span class="sxs-lookup"><span data-stu-id="01a44-144">Version</span></span><br/> | <span data-ttu-id="01a44-145">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="01a44-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="01a44-146">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01a44-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="01a44-147">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="01a44-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="01a44-148">DLL</span><span class="sxs-lookup"><span data-stu-id="01a44-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="01a44-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a44-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="01a44-150">IID</span><span class="sxs-lookup"><span data-stu-id="01a44-150">IID</span></span><br/>     | <span data-ttu-id="01a44-151">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="01a44-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="01a44-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01a44-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a44-153">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="01a44-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="01a44-154">**мсикуерифеатурестатикс**</span><span class="sxs-lookup"><span data-stu-id="01a44-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="01a44-155">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="01a44-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




