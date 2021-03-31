---
description: Метод Кскуеримедиумс извлекает средние, поддерживаемые ПИН-кодом.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Метод Икспин:: Кскуеримедиумс (Кспрокси. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806082"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="b2c4b-103">Метод Икспин:: Кскуеримедиумс</span><span class="sxs-lookup"><span data-stu-id="b2c4b-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="b2c4b-104">`KsQueryMediums`Метод извлекает средние, поддерживаемые ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="b2c4b-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2c4b-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="b2c4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c4b-107">*ппми* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2c4b-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c4b-108">Адрес указателя на структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b2c4b-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c4b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2c4b-109">Return value</span></span>

<span data-ttu-id="b2c4b-110">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b2c4b-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b2c4b-111">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2c4b-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c4b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2c4b-112">Remarks</span></span>

<span data-ttu-id="b2c4b-113">Этот метод возвращает выделенную задачей структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) , за которой следует ноль или более структур [**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) .</span><span class="sxs-lookup"><span data-stu-id="b2c4b-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="b2c4b-114">Элемент **Count** в структуре **\_ элемента Ксмултипле** указывает количество структур **регпинмедиум** .</span><span class="sxs-lookup"><span data-stu-id="b2c4b-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="b2c4b-115">Каждая структура **регпинмедиум** определяет средний уровень, поддерживаемый ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="b2c4b-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="b2c4b-116">Вызывающий объект должен освобождать возвращаемые структуры с помощью функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="b2c4b-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="b2c4b-117">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="b2c4b-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="b2c4b-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="b2c4b-118">Examples</span></span>

<span data-ttu-id="b2c4b-119">Следующая вспомогательная функция пытается сопоставить ПИН-код с указанным носителем.</span><span class="sxs-lookup"><span data-stu-id="b2c4b-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="b2c4b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b2c4b-120">Requirements</span></span>



| <span data-ttu-id="b2c4b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b2c4b-121">Requirement</span></span> | <span data-ttu-id="b2c4b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b2c4b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c4b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2c4b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c4b-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2c4b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2c4b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2c4b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c4b-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2c4b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2c4b-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2c4b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c4b-128"><dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2c4b-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="b2c4b-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2c4b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2c4b-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2c4b-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c4b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2c4b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c4b-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="b2c4b-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="b2c4b-133">**Интерфейс Икспин**</span><span class="sxs-lookup"><span data-stu-id="b2c4b-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="b2c4b-134">Фильтры драйвера класса WDM</span><span class="sxs-lookup"><span data-stu-id="b2c4b-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




