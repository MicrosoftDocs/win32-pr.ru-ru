---
description: Метод Фрипропс освобождает ресурсы, выделенные методом Ипропертисеттер::. Вызовите этот метод после вызова метода "PROPS", передав ему структуры, возвращаемые методами PROPS.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Метод Ипропертисеттер:: Фрипропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675025"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="69bb8-104">Метод Ипропертисеттер:: Фрипропс</span><span class="sxs-lookup"><span data-stu-id="69bb8-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="69bb8-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="69bb8-105">\[Deprecated.</span></span> <span data-ttu-id="69bb8-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69bb8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="69bb8-107">`FreeProps`Метод освобождает ресурсы, выделенные методом [**ипропертисеттер:: "PROPS**](ipropertysetter-getprops.md) ".</span><span class="sxs-lookup"><span data-stu-id="69bb8-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="69bb8-108">Вызовите этот метод после вызова метода " **PROPS**", передав ему структуры, возвращаемые методами **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="69bb8-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bb8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69bb8-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="69bb8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="69bb8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bb8-111">*кпарамс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69bb8-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bb8-112">Число элементов в массиве *папарам* .</span><span class="sxs-lookup"><span data-stu-id="69bb8-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="69bb8-113">*папарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69bb8-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bb8-114">Указатель на массив структур [**\_ param Декстер**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="69bb8-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="69bb8-115">*павалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69bb8-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69bb8-116">Указатель на массив структур [**\_ значений Декстер**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="69bb8-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bb8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69bb8-117">Return value</span></span>

<span data-ttu-id="69bb8-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="69bb8-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69bb8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69bb8-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69bb8-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="69bb8-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="69bb8-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69bb8-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="69bb8-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="69bb8-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69bb8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="69bb8-123">Requirements</span></span>



| <span data-ttu-id="69bb8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="69bb8-124">Requirement</span></span> | <span data-ttu-id="69bb8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="69bb8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69bb8-126">Header</span><span class="sxs-lookup"><span data-stu-id="69bb8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="69bb8-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bb8-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="69bb8-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69bb8-128">Library</span></span><br/> | <dl> <span data-ttu-id="69bb8-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69bb8-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69bb8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69bb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bb8-131">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="69bb8-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="69bb8-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="69bb8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




