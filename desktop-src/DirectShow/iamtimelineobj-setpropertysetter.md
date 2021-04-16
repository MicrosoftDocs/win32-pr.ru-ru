---
description: Метод Сетпропертисеттер устанавливает метод задания свойства объекта. При подготовке к просмотру объекта сведения о свойствах, содержащиеся в методе задания свойств, применяются к объекту. Вызывайте этот метод для объектов перехода и эффектов.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Метод Иамтимелинеобж:: Сетпропертисеттер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676039"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="16e00-105">Метод Иамтимелинеобж:: Сетпропертисеттер</span><span class="sxs-lookup"><span data-stu-id="16e00-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="16e00-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="16e00-106">\[Deprecated.</span></span> <span data-ttu-id="16e00-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="16e00-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="16e00-108">`SetPropertySetter`Метод задает свойство метода для свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="16e00-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="16e00-109">При подготовке к просмотру объекта сведения о свойствах, содержащиеся в методе задания свойств, применяются к объекту.</span><span class="sxs-lookup"><span data-stu-id="16e00-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="16e00-110">Вызывайте этот метод для объектов перехода и эффектов.</span><span class="sxs-lookup"><span data-stu-id="16e00-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e00-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16e00-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="16e00-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e00-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e00-113">*неввал*</span><span class="sxs-lookup"><span data-stu-id="16e00-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="16e00-114">Указатель на интерфейс [**ипропертисеттер**](ipropertysetter.md) метода задания свойств.</span><span class="sxs-lookup"><span data-stu-id="16e00-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e00-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e00-115">Return value</span></span>

<span data-ttu-id="16e00-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="16e00-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16e00-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16e00-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e00-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e00-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="16e00-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="16e00-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="16e00-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16e00-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="16e00-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="16e00-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16e00-122">Требования</span><span class="sxs-lookup"><span data-stu-id="16e00-122">Requirements</span></span>



| <span data-ttu-id="16e00-123">Требование</span><span class="sxs-lookup"><span data-stu-id="16e00-123">Requirement</span></span> | <span data-ttu-id="16e00-124">Значение</span><span class="sxs-lookup"><span data-stu-id="16e00-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16e00-125">Header</span><span class="sxs-lookup"><span data-stu-id="16e00-125">Header</span></span><br/>  | <dl> <span data-ttu-id="16e00-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e00-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="16e00-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16e00-127">Library</span></span><br/> | <dl> <span data-ttu-id="16e00-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16e00-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e00-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16e00-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e00-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="16e00-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="16e00-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="16e00-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




