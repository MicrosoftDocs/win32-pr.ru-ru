---
description: Метод размещения \_ репликатекс указывает, сколько раз шаблон очистки реплицируется по горизонтали.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: 'Идкстжпег: метод ut_ReplicateX:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08d892619fe1e6f8222b40d45e634a350e4e9b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675401"
---
# <a name="idxtjpegput_replicatex-method"></a><span data-ttu-id="f6b59-103">Идкстжпег::p UT \_ репликатекс метод</span><span class="sxs-lookup"><span data-stu-id="f6b59-103">IDxtJpeg::put\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="f6b59-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f6b59-104">\[Deprecated.</span></span> <span data-ttu-id="f6b59-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6b59-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6b59-106">`put_ReplicateX`Метод указывает, сколько раз шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="f6b59-106">The `put_ReplicateX` method specifies the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6b59-107">Syntax</span></span>


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f6b59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6b59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b59-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6b59-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b59-110">Количество раз, когда шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="f6b59-110">The number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6b59-111">Return value</span></span>

<span data-ttu-id="f6b59-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f6b59-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6b59-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6b59-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b59-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6b59-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f6b59-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f6b59-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6b59-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6b59-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6b59-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f6b59-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6b59-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f6b59-118">Requirements</span></span>



| <span data-ttu-id="f6b59-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f6b59-119">Requirement</span></span> | <span data-ttu-id="f6b59-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f6b59-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b59-121">Header</span><span class="sxs-lookup"><span data-stu-id="f6b59-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f6b59-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6b59-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6b59-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6b59-123">Library</span></span><br/> | <dl> <span data-ttu-id="f6b59-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6b59-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b59-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6b59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b59-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="f6b59-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




