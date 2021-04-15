---
description: Метод Get получает свойство, определяемое идентификатором GUID набора свойств и ИДЕНТИФИКАТОРом свойства.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Метод Икспропертисет:: Get (Кспрокси. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495075"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="b2065-103">Метод Икспропертисет:: Get</span><span class="sxs-lookup"><span data-stu-id="b2065-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="b2065-104">Метод **Get** получает свойство, ОПРЕДЕЛЯЕМое идентификатором GUID набора свойств и идентификатором свойства.</span><span class="sxs-lookup"><span data-stu-id="b2065-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2065-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2065-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="b2065-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2065-107">*гуидпропсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2065-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-108">Идентификатор GUID набора свойств.</span><span class="sxs-lookup"><span data-stu-id="b2065-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="b2065-109">*dwPropID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2065-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-110">Идентификатор свойства в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="b2065-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="b2065-111">*пинстанцедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2065-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-112">Указатель на массив байтов, содержащий данные экземпляра для свойства.</span><span class="sxs-lookup"><span data-stu-id="b2065-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="b2065-113">*кбинстанцедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2065-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-114">Размер массива, заданного в *пинстанцедата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="b2065-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b2065-115">*ппропдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2065-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-116">Указатель на массив байтов, который получает данные свойства.</span><span class="sxs-lookup"><span data-stu-id="b2065-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="b2065-117">*кбпропдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2065-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-118">Размер массива, заданного в *ппропдата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="b2065-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b2065-119">*пкбретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2065-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2065-120">Получает число байтов, которые метод копирует в массив *ппропдата* .</span><span class="sxs-lookup"><span data-stu-id="b2065-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2065-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2065-121">Return value</span></span>

<span data-ttu-id="b2065-122">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2065-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b2065-123">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="b2065-123">Possible values include the following.</span></span>



| <span data-ttu-id="b2065-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b2065-124">Return code</span></span>                                                                                              | <span data-ttu-id="b2065-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b2065-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2065-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b2065-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="b2065-127">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b2065-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b2065-128"><dt>**\_набор свойств \_ E \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="b2065-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="b2065-129">Набор свойств не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2065-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="b2065-130"><dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt></span><span class="sxs-lookup"><span data-stu-id="b2065-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="b2065-131">Идентификатор свойства не поддерживается для указанного набора свойств.</span><span class="sxs-lookup"><span data-stu-id="b2065-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2065-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2065-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2065-133">Другой интерфейс с таким именем существует в файле заголовка дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="b2065-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="b2065-134">Два интерфейса несовместимы.</span><span class="sxs-lookup"><span data-stu-id="b2065-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="b2065-135">Интерфейс [иксконтрол](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , документированный в пакете DDK по DirectShow, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="b2065-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="b2065-136">Чтобы получить свойство, выделите буфер, который затем будет заполняться этим методом.</span><span class="sxs-lookup"><span data-stu-id="b2065-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="b2065-137">Чтобы определить необходимый размер буфера, укажите **значение NULL** для *ппропдата* и ноль (0) для *кбпропдата*.</span><span class="sxs-lookup"><span data-stu-id="b2065-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="b2065-138">Этот метод возвращает необходимый размер буфера в *пкбретурнед*.</span><span class="sxs-lookup"><span data-stu-id="b2065-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="b2065-139">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="b2065-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="b2065-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="b2065-140">Examples</span></span>

<span data-ttu-id="b2065-141">В следующем примере запрашивается ПИН-код для своей категории ПИН-кода путем извлечения свойства **ампроперти \_ PIN \_ Category** .</span><span class="sxs-lookup"><span data-stu-id="b2065-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="b2065-142">(См. раздел [закрепить набор свойств](pin-property-set.md).)</span><span class="sxs-lookup"><span data-stu-id="b2065-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b2065-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b2065-143">Requirements</span></span>



| <span data-ttu-id="b2065-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b2065-144">Requirement</span></span> | <span data-ttu-id="b2065-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b2065-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2065-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2065-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b2065-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2065-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2065-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2065-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b2065-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2065-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2065-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2065-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2065-151"><dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2065-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="b2065-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2065-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2065-153"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2065-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2065-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2065-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2065-155">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="b2065-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="b2065-156">**Интерфейс Икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="b2065-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="b2065-157">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="b2065-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
