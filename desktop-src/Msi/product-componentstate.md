---
description: Свойство Компонентстате — это состояние установки компонента для экземпляра данного продукта. Это свойство вызывает Мсикуерикомпонентстате с ProductCode, а также контекстом объекта.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Метод Product. Компонентстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652061"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="75d8c-103">Метод Product. Компонентстате</span><span class="sxs-lookup"><span data-stu-id="75d8c-103">Product.ComponentState method</span></span>

<span data-ttu-id="75d8c-104">Свойство **компонентстате** — это состояние установки компонента для экземпляра данного продукта.</span><span class="sxs-lookup"><span data-stu-id="75d8c-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="75d8c-105">Это свойство вызывает [**мсикуерикомпонентстате**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)с ProductCode, а также контекстом объекта.</span><span class="sxs-lookup"><span data-stu-id="75d8c-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="75d8c-106">Идентификатор GUID компонента указывается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="75d8c-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75d8c-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="75d8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75d8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d8c-109">*Идентификатор*</span><span class="sxs-lookup"><span data-stu-id="75d8c-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="75d8c-110">Код компонента GUID компонента, найденный в столбце ComponentID [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="75d8c-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d8c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75d8c-111">Return value</span></span>

<span data-ttu-id="75d8c-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="75d8c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d8c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75d8c-113">Remarks</span></span>

<span data-ttu-id="75d8c-114">Если вызов будет выполнен, свойство будет содержать значение **типа DWORD**.</span><span class="sxs-lookup"><span data-stu-id="75d8c-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="75d8c-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="75d8c-115">State</span></span>                | <span data-ttu-id="75d8c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="75d8c-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="75d8c-117">INSTALLSTATE \_ локальный</span><span class="sxs-lookup"><span data-stu-id="75d8c-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="75d8c-118">Компонент устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="75d8c-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="75d8c-119">\_источник InstallState</span><span class="sxs-lookup"><span data-stu-id="75d8c-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="75d8c-120">Компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="75d8c-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="75d8c-121">Если вызов завершается неудачей, свойство содержит код ошибки из [**мсикуерикомпонентстате**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="75d8c-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="75d8c-122">Ошибка</span><span class="sxs-lookup"><span data-stu-id="75d8c-122">Error</span></span>                     | <span data-ttu-id="75d8c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="75d8c-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d8c-124">Ошибка \_ отказа в доступе \_</span><span class="sxs-lookup"><span data-stu-id="75d8c-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="75d8c-125">Вызывающий процесс должен иметь права администратора для получения сведений для пользователя, отличного от текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="75d8c-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="75d8c-126">Ошибка \_ неправильной \_ конфигурации</span><span class="sxs-lookup"><span data-stu-id="75d8c-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="75d8c-127">Данные конфигурации повреждены.</span><span class="sxs-lookup"><span data-stu-id="75d8c-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="75d8c-128">Ошибка \_ недопустимого \_ параметра</span><span class="sxs-lookup"><span data-stu-id="75d8c-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="75d8c-129">Функции передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="75d8c-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="75d8c-130">Ошибка при \_ успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="75d8c-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="75d8c-131">Функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="75d8c-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="75d8c-132">Ошибка \_ неизвестного \_ компонента</span><span class="sxs-lookup"><span data-stu-id="75d8c-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="75d8c-133">Идентификатор компонента не определяет известный компонент.</span><span class="sxs-lookup"><span data-stu-id="75d8c-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="75d8c-134">Ошибка \_ неизвестного \_ продукта</span><span class="sxs-lookup"><span data-stu-id="75d8c-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="75d8c-135">Код продукта не определяет известный продукт.</span><span class="sxs-lookup"><span data-stu-id="75d8c-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="75d8c-136">Ошибка \_ \_ при выполнении функции</span><span class="sxs-lookup"><span data-stu-id="75d8c-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="75d8c-137">Непредвиденный внутренний сбой.</span><span class="sxs-lookup"><span data-stu-id="75d8c-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="75d8c-138">Требования</span><span class="sxs-lookup"><span data-stu-id="75d8c-138">Requirements</span></span>



| <span data-ttu-id="75d8c-139">Требование</span><span class="sxs-lookup"><span data-stu-id="75d8c-139">Requirement</span></span> | <span data-ttu-id="75d8c-140">Значение</span><span class="sxs-lookup"><span data-stu-id="75d8c-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d8c-141">Версия</span><span class="sxs-lookup"><span data-stu-id="75d8c-141">Version</span></span><br/> | <span data-ttu-id="75d8c-142">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75d8c-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="75d8c-143">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75d8c-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="75d8c-144">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="75d8c-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="75d8c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="75d8c-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="75d8c-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d8c-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="75d8c-147">IID</span><span class="sxs-lookup"><span data-stu-id="75d8c-147">IID</span></span><br/>     | <span data-ttu-id="75d8c-148">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="75d8c-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="75d8c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75d8c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d8c-150">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="75d8c-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="75d8c-151">**мсикуерикомпонентстате**</span><span class="sxs-lookup"><span data-stu-id="75d8c-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="75d8c-152">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="75d8c-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




