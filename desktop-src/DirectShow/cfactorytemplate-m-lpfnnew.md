---
description: Указатель на функцию, которая создает экземпляр объекта.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Элемент Кфакторитемплате:: m_lpfnNew (Комбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668819"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="933d4-103">Элемент Кфакторитемплате:: m \_ лпфннев</span><span class="sxs-lookup"><span data-stu-id="933d4-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="933d4-104">Указатель на функцию, которая создает экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="933d4-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="933d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="933d4-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="933d4-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="933d4-106">Remarks</span></span>

<span data-ttu-id="933d4-107">В библиотеке DLL Объявите статическую функцию, которая возвращает указатель на новый экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="933d4-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="933d4-108">В шаблоне фабрики задайте в качестве значения переменной члена **m \_ лпфннев** адрес этой статической функции.</span><span class="sxs-lookup"><span data-stu-id="933d4-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="933d4-109">Тип указателя функции — [**лпфнневкомобжект**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="933d4-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="933d4-110">В следующем примере показана типичная функция для **m \_ лпфннев**:</span><span class="sxs-lookup"><span data-stu-id="933d4-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="933d4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="933d4-111">Requirements</span></span>



| <span data-ttu-id="933d4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="933d4-112">Requirement</span></span> | <span data-ttu-id="933d4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="933d4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="933d4-114">Header</span><span class="sxs-lookup"><span data-stu-id="933d4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="933d4-115"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="933d4-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="933d4-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="933d4-116">Library</span></span><br/> | <dl> <span data-ttu-id="933d4-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="933d4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933d4-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="933d4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933d4-119">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="933d4-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




