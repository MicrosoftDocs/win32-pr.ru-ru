---
description: Метод Креатимптиноде создает новый объект Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Метод Иамтимелине:: Креатимптиноде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675292"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="f7f27-103">Метод Иамтимелине:: Креатимптиноде</span><span class="sxs-lookup"><span data-stu-id="f7f27-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="f7f27-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f7f27-104">\[Deprecated.</span></span> <span data-ttu-id="f7f27-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f7f27-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f7f27-106">`CreateEmptyNode`Метод создает новый объект временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f7f27-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="f7f27-107">Этот метод используется для создания объектов временной шкалы, а не функции **CoCreateInstance** , поскольку этот метод выполняет важные процедуры инициализации.</span><span class="sxs-lookup"><span data-stu-id="f7f27-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="f7f27-108">Каждый объект, созданный этим методом, поддерживает по крайней мере интерфейс [**иамтимелинеобж**](iamtimelineobj.md) , а также другие интерфейсы, относящиеся к этому типу объекта.</span><span class="sxs-lookup"><span data-stu-id="f7f27-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f27-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7f27-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="f7f27-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7f27-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f27-111">*ппобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7f27-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7f27-112">Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) нового объекта.</span><span class="sxs-lookup"><span data-stu-id="f7f27-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f7f27-113">*Тип*</span><span class="sxs-lookup"><span data-stu-id="f7f27-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f27-114">Элемент перечисляемого типа " [**\_ основной \_ тип временной шкалы**](timeline-major-type.md) ", указывающий тип создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f7f27-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f27-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7f27-115">Return value</span></span>

<span data-ttu-id="f7f27-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f7f27-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7f27-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7f27-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f27-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7f27-118">Remarks</span></span>

<span data-ttu-id="f7f27-119">Не добавляйте новый объект в другой экземпляр временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f7f27-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="f7f27-120">Каждый объект на временной шкале должен быть создан этой временной шкалой.</span><span class="sxs-lookup"><span data-stu-id="f7f27-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="f7f27-121">Если метод завершается успешно, интерфейс [**иамтимелинеобж**](iamtimelineobj.md) , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="f7f27-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="f7f27-122">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="f7f27-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="f7f27-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f7f27-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f7f27-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7f27-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f7f27-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f7f27-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7f27-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f7f27-126">Requirements</span></span>



| <span data-ttu-id="f7f27-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f7f27-127">Requirement</span></span> | <span data-ttu-id="f7f27-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f7f27-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f27-129">Header</span><span class="sxs-lookup"><span data-stu-id="f7f27-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f7f27-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7f27-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f7f27-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7f27-131">Library</span></span><br/> | <dl> <span data-ttu-id="f7f27-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7f27-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f27-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7f27-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f27-134">**Интерфейс Иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="f7f27-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="f7f27-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f7f27-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




