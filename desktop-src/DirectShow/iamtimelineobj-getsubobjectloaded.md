---
description: Метод Жетсубобжектлоадед определяет, установлен ли указатель на подобъект.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'Метод Иамтимелинеобж:: Жетсубобжектлоадед (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685335"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="f0bd1-103">Метод Иамтимелинеобж:: Жетсубобжектлоадед</span><span class="sxs-lookup"><span data-stu-id="f0bd1-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="f0bd1-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-104">\[Deprecated.</span></span> <span data-ttu-id="f0bd1-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f0bd1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0bd1-106">`GetSubObjectLoaded`Метод определяет, установлен ли указатель на подобъект.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bd1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0bd1-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f0bd1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0bd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bd1-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f0bd1-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f0bd1-110">Получает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-110">Receives a Boolean value.</span></span> <span data-ttu-id="f0bd1-111">Если значение равно **true**, то был установлен указатель на подобъект.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="f0bd1-112">Если **значение равно false**, то указатель не был задан.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bd1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0bd1-113">Return value</span></span>

<span data-ttu-id="f0bd1-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0bd1-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0bd1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0bd1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0bd1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0bd1-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0bd1-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0bd1-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0bd1-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f0bd1-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0bd1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f0bd1-120">Requirements</span></span>



| <span data-ttu-id="f0bd1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f0bd1-121">Requirement</span></span> | <span data-ttu-id="f0bd1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f0bd1-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bd1-123">Header</span><span class="sxs-lookup"><span data-stu-id="f0bd1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f0bd1-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd1-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0bd1-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f0bd1-125">Library</span></span><br/> | <dl> <span data-ttu-id="f0bd1-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd1-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0bd1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0bd1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bd1-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="f0bd1-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f0bd1-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="f0bd1-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




