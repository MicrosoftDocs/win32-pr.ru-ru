---
description: Метод Еффектжетприорити извлекает уровень приоритета результата. Для данного объекта механизм визуализации применяет эффекты в порядке приоритета, начиная с нулевого уровня приоритета.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Метод Иамтимелиниффект:: Еффектжетприорити (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689502"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="0931c-104">Метод Иамтимелиниффект:: Еффектжетприорити</span><span class="sxs-lookup"><span data-stu-id="0931c-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="0931c-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0931c-105">\[Deprecated.</span></span> <span data-ttu-id="0931c-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0931c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0931c-107">`EffectGetPriority`Метод получает уровень приоритета результата.</span><span class="sxs-lookup"><span data-stu-id="0931c-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="0931c-108">Для данного объекта механизм визуализации применяет эффекты в порядке приоритета, начиная с нулевого уровня приоритета.</span><span class="sxs-lookup"><span data-stu-id="0931c-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="0931c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0931c-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0931c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0931c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0931c-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="0931c-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0931c-112">Получает уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="0931c-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0931c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0931c-113">Return value</span></span>

<span data-ttu-id="0931c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0931c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0931c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0931c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0931c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0931c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0931c-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0931c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0931c-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0931c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0931c-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0931c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0931c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0931c-120">Requirements</span></span>



| <span data-ttu-id="0931c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0931c-121">Requirement</span></span> | <span data-ttu-id="0931c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0931c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0931c-123">Header</span><span class="sxs-lookup"><span data-stu-id="0931c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0931c-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0931c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0931c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0931c-125">Library</span></span><br/> | <dl> <span data-ttu-id="0931c-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0931c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0931c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0931c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0931c-128">**Интерфейс Иамтимелиниффект**</span><span class="sxs-lookup"><span data-stu-id="0931c-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="0931c-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0931c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




