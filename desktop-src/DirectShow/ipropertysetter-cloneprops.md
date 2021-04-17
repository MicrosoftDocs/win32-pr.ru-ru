---
description: Метод Клонепропс копирует набор свойств из этого метода задания свойств и добавляет их в новый метод задания свойств.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Метод Ипропертисеттер:: Клонепропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685218"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="22979-103">Метод Ипропертисеттер:: Клонепропс</span><span class="sxs-lookup"><span data-stu-id="22979-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="22979-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="22979-104">\[Deprecated.</span></span> <span data-ttu-id="22979-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22979-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22979-106">`CloneProps`Метод копирует набор свойств из этого метода задания свойств и добавляет их в новый метод задания свойств.</span><span class="sxs-lookup"><span data-stu-id="22979-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="22979-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22979-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="22979-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22979-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22979-109">*ппсеттер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22979-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22979-110">Получает указатель на интерфейс **ипропертисеттер** нового метода задания свойства.</span><span class="sxs-lookup"><span data-stu-id="22979-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="22979-111">*ртстарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22979-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22979-112">Время начала диапазона значений для клонирования в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="22979-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="22979-113">*ртстоп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22979-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22979-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="22979-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22979-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22979-115">Return value</span></span>

<span data-ttu-id="22979-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="22979-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22979-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22979-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22979-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22979-118">Remarks</span></span>

<span data-ttu-id="22979-119">Клонированием будут только значения, попадающие после указанного времени начала.</span><span class="sxs-lookup"><span data-stu-id="22979-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="22979-120">Время на клонированных значениях затем корректируется относительно времени начала.</span><span class="sxs-lookup"><span data-stu-id="22979-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="22979-121">Например, если *ртстарт* равен 20000000 (2 секунды), то значение в момент времени 30000000 (3 секунды) клонируется с временем 10000000 (1 секунда).</span><span class="sxs-lookup"><span data-stu-id="22979-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="22979-122">Наконец, каждому клонированному свойству присваивается начальное значение, равное значению исходного свойства в момент начала (при необходимости в правильной интерполяции).</span><span class="sxs-lookup"><span data-stu-id="22979-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="22979-123">Фактически данные свойства разбиваются на указанное время начала.</span><span class="sxs-lookup"><span data-stu-id="22979-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="22979-124">Если метод завершается успешно, интерфейс [**ипропертисеттер**](ipropertysetter.md) , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="22979-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="22979-125">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="22979-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="22979-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="22979-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22979-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22979-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22979-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="22979-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22979-129">Требования</span><span class="sxs-lookup"><span data-stu-id="22979-129">Requirements</span></span>



| <span data-ttu-id="22979-130">Требование</span><span class="sxs-lookup"><span data-stu-id="22979-130">Requirement</span></span> | <span data-ttu-id="22979-131">Значение</span><span class="sxs-lookup"><span data-stu-id="22979-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22979-132">Header</span><span class="sxs-lookup"><span data-stu-id="22979-132">Header</span></span><br/>  | <dl> <span data-ttu-id="22979-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="22979-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22979-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22979-134">Library</span></span><br/> | <dl> <span data-ttu-id="22979-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22979-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22979-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22979-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22979-137">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="22979-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="22979-138">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="22979-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




