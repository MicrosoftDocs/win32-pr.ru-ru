---
description: Метод Set задает свойство, определяемое идентификатором GUID набора свойств и ИДЕНТИФИКАТОРом свойства.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Метод Икспропертисет:: Set (Кспрокси. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416688"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="59152-103">Метод Икспропертисет:: Set</span><span class="sxs-lookup"><span data-stu-id="59152-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="59152-104">`Set`Метод задает свойство, определяемое идентификатором GUID набора свойств и идентификатором свойства.</span><span class="sxs-lookup"><span data-stu-id="59152-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="59152-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59152-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="59152-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59152-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59152-107">*гуидпропсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-108">Идентификатор GUID набора свойств.</span><span class="sxs-lookup"><span data-stu-id="59152-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="59152-109">*dwPropID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-110">Идентификатор свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="59152-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="59152-111">*пинстанцедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-112">Указатель на буфер, содержащий данные экземпляра для свойства.</span><span class="sxs-lookup"><span data-stu-id="59152-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="59152-113">*кбинстанцедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-114">Размер буфера *пинстанцедата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="59152-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="59152-115">*ппропдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-116">Указатель на буфер, содержащий значение свойства.</span><span class="sxs-lookup"><span data-stu-id="59152-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="59152-117">*кбпропдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59152-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59152-118">Сисе буфера *ппропдата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="59152-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59152-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59152-119">Return value</span></span>

<span data-ttu-id="59152-120">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59152-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="59152-121">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="59152-121">Possible values include the following.</span></span>



| <span data-ttu-id="59152-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="59152-122">Return code</span></span>                                                                                              | <span data-ttu-id="59152-123">Описание</span><span class="sxs-lookup"><span data-stu-id="59152-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59152-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="59152-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="59152-125">Успешно.</span><span class="sxs-lookup"><span data-stu-id="59152-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="59152-126"><dt>**\_набор свойств \_ E \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="59152-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="59152-127">Набор свойств не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="59152-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="59152-128"><dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="59152-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="59152-129">Идентификатор свойства не поддерживается для указанного набора свойств.</span><span class="sxs-lookup"><span data-stu-id="59152-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59152-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59152-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59152-131">Другой интерфейс с таким именем существует в файле заголовка дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="59152-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="59152-132">Два интерфейса несовместимы.</span><span class="sxs-lookup"><span data-stu-id="59152-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="59152-133">Интерфейс **иксконтрол** , документированный в пакете DDK по DirectShow, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="59152-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="59152-134">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="59152-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="59152-135">Требования</span><span class="sxs-lookup"><span data-stu-id="59152-135">Requirements</span></span>



| <span data-ttu-id="59152-136">Требование</span><span class="sxs-lookup"><span data-stu-id="59152-136">Requirement</span></span> | <span data-ttu-id="59152-137">Значение</span><span class="sxs-lookup"><span data-stu-id="59152-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59152-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59152-138">Minimum supported client</span></span><br/> | <span data-ttu-id="59152-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59152-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="59152-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59152-140">Minimum supported server</span></span><br/> | <span data-ttu-id="59152-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59152-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59152-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="59152-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="59152-143"><dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="59152-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="59152-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59152-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="59152-145"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59152-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59152-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59152-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59152-147">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="59152-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="59152-148">**Интерфейс Икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="59152-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="59152-149">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="59152-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




