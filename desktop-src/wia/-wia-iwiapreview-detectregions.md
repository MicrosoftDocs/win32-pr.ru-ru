---
description: 'Вызывает фильтр сегментации драйвера и передает в фильтр нефильтрованное изображение, кэшированное методом Ивиапревиев:: Жетневпревиев.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: 'Ивиапревиев: метод:D Етектрегионс (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263135"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="288e3-103">Ивиапревиев: метод:D Етектрегионс</span><span class="sxs-lookup"><span data-stu-id="288e3-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="288e3-104">Вызывает фильтр сегментации драйвера и передает в фильтр нефильтрованное изображение, кэшированное методом [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="288e3-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="288e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="288e3-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="288e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="288e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288e3-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="288e3-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="288e3-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="288e3-108">Type: **LONG**</span></span>

<span data-ttu-id="288e3-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="288e3-109">Not used.</span></span> <span data-ttu-id="288e3-110">Установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="288e3-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288e3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="288e3-111">Return value</span></span>

<span data-ttu-id="288e3-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="288e3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="288e3-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="288e3-113">This method can return one of these values.</span></span>



| <span data-ttu-id="288e3-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="288e3-114">Return code</span></span>                                                                               | <span data-ttu-id="288e3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="288e3-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="288e3-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="288e3-117">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="288e3-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="288e3-118"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="288e3-119">Драйвер не поддерживает сегментацию.</span><span class="sxs-lookup"><span data-stu-id="288e3-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="288e3-120"><dt>**ином**</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="288e3-121">Стандартный код ошибки COM.</span><span class="sxs-lookup"><span data-stu-id="288e3-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="288e3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="288e3-122">Remarks</span></span>

<span data-ttu-id="288e3-123">Приложение должно вызвать метод [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md) перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="288e3-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="288e3-124">Когда компонент предварительной версии Windows Image (WIA) 2,0 Preview вызывает **ивиапревиев::D етектрегионс**, он вызывает фильтр сегментации драйвера и передает интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) , который ранее был передан [**ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="288e3-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="288e3-125">Он также передает внутренне кэшированное изображение в фильтр.</span><span class="sxs-lookup"><span data-stu-id="288e3-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="288e3-126">Фильтр сегментации использует кэшированный образ для создания дочерних экстентов.</span><span class="sxs-lookup"><span data-stu-id="288e3-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="288e3-127">Если приложение изменяет любые свойства интерфейса [**IWiaItem2**](-wia-iwiaitem2.md) после вызова [**Ивиапревиев:: жетневпревиев**](-wia-iwiapreview-getnewpreview.md), исходные свойства необходимо восстановить до того, как приложение вызовет **ивиапревиев::D етектрегионс**.</span><span class="sxs-lookup"><span data-stu-id="288e3-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="288e3-128">Используйте [**жетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) и [**сетпропертистреам**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) для восстановления исходных свойств.</span><span class="sxs-lookup"><span data-stu-id="288e3-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="288e3-129">**Ивиапревиев::D етектрегионс** используется для определения подобластей кэшированного изображения.</span><span class="sxs-lookup"><span data-stu-id="288e3-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="288e3-130">Для каждой обнаруженной вложенной области в интерфейсе [**IWiaItem2**](-wia-iwiaitem2.md) создается новый дочерний элемент WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="288e3-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="288e3-131">Для каждого дочернего элемента фильтр сегментации должен задать значения для следующих свойств WIA 2,0: WIA- \_ IP \_ КСПОС, WIA- \_ адресов \_ ИПОС, WIA-пакетов \_ \_ ксекстент и WIA-пакетов \_ \_ екстент.</span><span class="sxs-lookup"><span data-stu-id="288e3-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="288e3-132">Более расширенный фильтр устанавливает другие свойства WIA 2,0, такие как IP- \_ адреса WIA, \_ деравномерное смещение \_ X и WIA \_ \_ \_ , если драйвер поддерживает отмену наклона.</span><span class="sxs-lookup"><span data-stu-id="288e3-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="288e3-133">Кспос IP-адресов WIA \_ \_ , WIA-пакетов \_ \_ ИПОС, WIA-пакетов \_ \_ ксекстент и WIA- \_ IP \_ екстент Properties представляют ограничивающий прямоугольник сканируемой области.</span><span class="sxs-lookup"><span data-stu-id="288e3-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="288e3-134">Драйвер может не поддерживать сегментацию.</span><span class="sxs-lookup"><span data-stu-id="288e3-134">The driver might not support segmentation.</span></span> <span data-ttu-id="288e3-135">Перед вызовом **ивиапревиев::D етектрегионс** приложение обычно проверяет, поддерживает ли драйвер \_ \_ свойство сегментации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="288e3-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="288e3-136">Если свойство не реализовано, сегментация не поддерживается и **ивиапревиев::D етектрегионс** завершает работу и возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="288e3-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="288e3-137">Приложение должно очистить дочерние элементы, созданные путем вызова **ивиапревиев::D етектрегионс**.</span><span class="sxs-lookup"><span data-stu-id="288e3-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="288e3-138">Например, если приложение выполняет дополнительный вызов **ивиапревиев::D етектрегионс** для того же элемента, он должен очистить предыдущие дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="288e3-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="288e3-139">Требования</span><span class="sxs-lookup"><span data-stu-id="288e3-139">Requirements</span></span>



| <span data-ttu-id="288e3-140">Требование</span><span class="sxs-lookup"><span data-stu-id="288e3-140">Requirement</span></span> | <span data-ttu-id="288e3-141">Значение</span><span class="sxs-lookup"><span data-stu-id="288e3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="288e3-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="288e3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="288e3-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="288e3-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="288e3-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="288e3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="288e3-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="288e3-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="288e3-146">Header</span><span class="sxs-lookup"><span data-stu-id="288e3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="288e3-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="288e3-148">IDL</span><span class="sxs-lookup"><span data-stu-id="288e3-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="288e3-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="288e3-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




