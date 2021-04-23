---
description: Метод Куерисуппортед определяет, поддерживает ли объект заданный набор свойств.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Метод Икспропертисет:: Куерисуппортед (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262382"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="7da49-103">Метод Икспропертисет:: Куерисуппортед</span><span class="sxs-lookup"><span data-stu-id="7da49-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="7da49-104">`QuerySupported`Метод определяет, поддерживает ли объект заданный набор свойств.</span><span class="sxs-lookup"><span data-stu-id="7da49-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7da49-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="7da49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da49-107">*гуидпропсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7da49-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da49-108">Идентификатор GUID набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7da49-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="7da49-109">*dwPropID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7da49-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da49-110">Идентификатор свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="7da49-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="7da49-111">*птипесуппорт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7da49-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7da49-112">Указатель на значение, в котором сохраняются флаги, указывающие на поддержку, предоставляемую драйвером.</span><span class="sxs-lookup"><span data-stu-id="7da49-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="7da49-113">Поддерживаются следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7da49-113">Supported flags include the following.</span></span>



| <span data-ttu-id="7da49-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7da49-114">Value</span></span>                    | <span data-ttu-id="7da49-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7da49-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da49-116">\_Поддержка кспроперти \_ Get</span><span class="sxs-lookup"><span data-stu-id="7da49-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="7da49-117">Свойство можно получить, вызвав метод [**икспропертисет:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="7da49-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="7da49-118">\_набор поддержки \_ кспроперти</span><span class="sxs-lookup"><span data-stu-id="7da49-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="7da49-119">Свойство можно изменить, вызвав [**икспропертисет:: Set**](ikspropertyset-set.md).</span><span class="sxs-lookup"><span data-stu-id="7da49-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da49-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7da49-120">Return value</span></span>

<span data-ttu-id="7da49-121">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7da49-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7da49-122">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="7da49-122">Possible values include the following.</span></span>



| <span data-ttu-id="7da49-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7da49-123">Return code</span></span>                                                                                              | <span data-ttu-id="7da49-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7da49-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7da49-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="7da49-126">Поддерживается сочетание указанного набора свойств и идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="7da49-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="7da49-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="7da49-128">Набор свойств не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7da49-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="7da49-129"><dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="7da49-130">Идентификатор свойства не поддерживается для указанного набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7da49-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="7da49-131"><dt>**\_набор свойств \_ E \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="7da49-132">Набор свойств не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7da49-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="7da49-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7da49-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7da49-134">Другой интерфейс с таким именем существует в файле заголовка дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="7da49-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="7da49-135">Два интерфейса несовместимы.</span><span class="sxs-lookup"><span data-stu-id="7da49-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="7da49-136">Интерфейс **иксконтрол** , документированный в пакете DDK по DirectShow, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="7da49-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="7da49-137">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="7da49-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da49-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7da49-138">Requirements</span></span>



| <span data-ttu-id="7da49-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7da49-139">Requirement</span></span> | <span data-ttu-id="7da49-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7da49-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da49-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7da49-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7da49-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7da49-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="7da49-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7da49-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7da49-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7da49-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="7da49-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7da49-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da49-146"><dt>KS. h; </dt> <dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="7da49-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7da49-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="7da49-148"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7da49-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="7da49-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da49-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da49-150">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="7da49-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="7da49-151">**Интерфейс Икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="7da49-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="7da49-152">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="7da49-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




