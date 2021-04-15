---
description: 'Метод GetCutPoint2 извлекает вырезанную точку. Этот метод эквивалентен Иамтимелинетранс:: Жеткутпоинт, но принимает значение РЕФТИМЕ.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'Метод Иамтимелинетранс:: GetCutPoint2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689448"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="51c4f-104">Метод Иамтимелинетранс:: GetCutPoint2</span><span class="sxs-lookup"><span data-stu-id="51c4f-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="51c4f-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="51c4f-105">\[Deprecated.</span></span> <span data-ttu-id="51c4f-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51c4f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51c4f-107">`GetCutPoint2`Метод извлекает вырезанную точку.</span><span class="sxs-lookup"><span data-stu-id="51c4f-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="51c4f-108">Этот метод эквивалентен [**иамтимелинетранс:: жеткутпоинт**](iamtimelinetrans-getcutpoint.md), но принимает значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="51c4f-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c4f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51c4f-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="51c4f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="51c4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c4f-111">*птлтиме*</span><span class="sxs-lookup"><span data-stu-id="51c4f-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="51c4f-112">Получает вырезанную точку относительно времени начала перехода в секундах.</span><span class="sxs-lookup"><span data-stu-id="51c4f-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c4f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51c4f-113">Return value</span></span>

<span data-ttu-id="51c4f-114">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="51c4f-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="51c4f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="51c4f-115">Return code</span></span>                                                                               | <span data-ttu-id="51c4f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="51c4f-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51c4f-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="51c4f-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="51c4f-118">Не задана вырезанная точка.</span><span class="sxs-lookup"><span data-stu-id="51c4f-118">The cut point was not set.</span></span> <span data-ttu-id="51c4f-119">Возвращаемое значение является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51c4f-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="51c4f-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="51c4f-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="51c4f-121">Для вырезанной точки задано значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51c4f-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="51c4f-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="51c4f-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="51c4f-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="51c4f-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="51c4f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51c4f-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="51c4f-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="51c4f-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="51c4f-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51c4f-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="51c4f-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="51c4f-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51c4f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="51c4f-128">Requirements</span></span>



| <span data-ttu-id="51c4f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="51c4f-129">Requirement</span></span> | <span data-ttu-id="51c4f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="51c4f-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51c4f-131">Header</span><span class="sxs-lookup"><span data-stu-id="51c4f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="51c4f-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c4f-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="51c4f-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51c4f-133">Library</span></span><br/> | <dl> <span data-ttu-id="51c4f-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51c4f-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c4f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51c4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c4f-136">**Интерфейс Иамтимелинетранс**</span><span class="sxs-lookup"><span data-stu-id="51c4f-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="51c4f-137">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="51c4f-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




