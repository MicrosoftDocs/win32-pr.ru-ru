---
description: '\_Структура фильтра амовиесетуп содержит сведения для регистрации фильтра.'
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Структура AMOVIESETUP_FILTER (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657838"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="5f66a-103">\_Структура фильтра амовиесетуп</span><span class="sxs-lookup"><span data-stu-id="5f66a-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="5f66a-104">Структура **\_ фильтра амовиесетуп** содержит сведения для регистрации фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f66a-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f66a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f66a-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="5f66a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5f66a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f66a-107">**Этому**</span><span class="sxs-lookup"><span data-stu-id="5f66a-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="5f66a-108">Идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f66a-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="5f66a-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="5f66a-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="5f66a-110">Имя фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f66a-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="5f66a-111">**двмерит**</span><span class="sxs-lookup"><span data-stu-id="5f66a-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="5f66a-112">Отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="5f66a-112">Filter merit.</span></span> <span data-ttu-id="5f66a-113">Используется интерфейсом [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) при создании графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f66a-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="5f66a-114">Список значений для получения списка недопустимых данных [см. в](merit.md)разделе.</span><span class="sxs-lookup"><span data-stu-id="5f66a-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f66a-115">**нпинс**</span><span class="sxs-lookup"><span data-stu-id="5f66a-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="5f66a-116">Число элементов в массиве *лппин* .</span><span class="sxs-lookup"><span data-stu-id="5f66a-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="5f66a-117">Если *лппин* имеет **значение NULL**, присвойте этому элементу значение 0.</span><span class="sxs-lookup"><span data-stu-id="5f66a-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f66a-118">**лппин**</span><span class="sxs-lookup"><span data-stu-id="5f66a-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="5f66a-119">Указатель на массив [**амовиесетупных структур \_ закрепления**](amoviesetup-pin.md) размера *нпинс*.</span><span class="sxs-lookup"><span data-stu-id="5f66a-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="5f66a-120">Каждый член этого массива описывает ПИН-код фильтра.</span><span class="sxs-lookup"><span data-stu-id="5f66a-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f66a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f66a-121">Remarks</span></span>

<span data-ttu-id="5f66a-122">Сведения об использовании этой структуры см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5f66a-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="5f66a-123">Используйте эту структуру только для фильтров, зарегистрированных в категории фильтра по умолчанию (CLSID \_ легациамфилтеркатегори).</span><span class="sxs-lookup"><span data-stu-id="5f66a-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="5f66a-124">Чтобы зарегистрировать фильтр в другой категории, используйте метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , как описано в разделе [Реализация DllRegisterServer](implementing-dllregisterserver.md).</span><span class="sxs-lookup"><span data-stu-id="5f66a-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="5f66a-125">Файл заголовка комбасе. h предоставляется [базовыми классами DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="5f66a-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f66a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5f66a-126">Requirements</span></span>



| <span data-ttu-id="5f66a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5f66a-127">Requirement</span></span> | <span data-ttu-id="5f66a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5f66a-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f66a-129">Header</span><span class="sxs-lookup"><span data-stu-id="5f66a-129">Header</span></span><br/> | <dl> <span data-ttu-id="5f66a-130"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f66a-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f66a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f66a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f66a-132">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f66a-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




