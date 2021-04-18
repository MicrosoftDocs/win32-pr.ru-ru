---
description: Не реализован.
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
ms.openlocfilehash: b8f0adee44de03560b347122a9c9cbdf500db897
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689150"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="54f3c-103">Метод Иамтимелинеобж:: Сетдиртиранже</span><span class="sxs-lookup"><span data-stu-id="54f3c-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="54f3c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="54f3c-104">\[Deprecated.</span></span> <span data-ttu-id="54f3c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54f3c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="54f3c-106">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="54f3c-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54f3c-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="54f3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="54f3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f3c-109">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="54f3c-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="54f3c-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="54f3c-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="54f3c-111">*Остановить*</span><span class="sxs-lookup"><span data-stu-id="54f3c-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="54f3c-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="54f3c-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f3c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54f3c-113">Return value</span></span>

<span data-ttu-id="54f3c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="54f3c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54f3c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54f3c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f3c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54f3c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54f3c-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="54f3c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="54f3c-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="54f3c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="54f3c-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="54f3c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54f3c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="54f3c-120">Requirements</span></span>



| <span data-ttu-id="54f3c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="54f3c-121">Requirement</span></span> | <span data-ttu-id="54f3c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="54f3c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54f3c-123">Header</span><span class="sxs-lookup"><span data-stu-id="54f3c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="54f3c-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f3c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="54f3c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54f3c-125">Library</span></span><br/> | <dl> <span data-ttu-id="54f3c-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54f3c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f3c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54f3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f3c-128">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="54f3c-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




