---
description: 'Метод Иамтимелинеобж:: Сетдиртиранже не реализован.'
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: 'Метод Иамтимелинеобж:: Сетдиртиранже (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3f70e5ba9d01733df154911c4f40d2b9d33776
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119492"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="7bc7b-103">Метод Иамтимелинеобж:: Сетдиртиранже</span><span class="sxs-lookup"><span data-stu-id="7bc7b-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="7bc7b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-104">\[Deprecated.</span></span> <span data-ttu-id="7bc7b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7bc7b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7bc7b-106">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc7b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bc7b-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="7bc7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bc7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc7b-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="7bc7b-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc7b-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7bc7b-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="7bc7b-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc7b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bc7b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bc7b-113">Return value</span></span>

<span data-ttu-id="7bc7b-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7bc7b-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7bc7b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc7b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="7bc7b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bc7b-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7bc7b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7bc7b-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7bc7b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7bc7b-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7bc7b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bc7b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7bc7b-120">Requirements</span></span>



| <span data-ttu-id="7bc7b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7bc7b-121">Requirement</span></span> | <span data-ttu-id="7bc7b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7bc7b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc7b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7bc7b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7bc7b-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bc7b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7bc7b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7bc7b-125">Library</span></span><br/> | <dl> <span data-ttu-id="7bc7b-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bc7b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bc7b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7bc7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc7b-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="7bc7b-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




