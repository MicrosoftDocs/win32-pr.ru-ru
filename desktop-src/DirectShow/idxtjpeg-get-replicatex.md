---
description: Метод Get \_ репликатекс извлекает количество раз, когда шаблон очистки реплицируется по горизонтали.
ms.assetid: 669a3bde-af8b-4d31-b914-41b71c95de1c
title: 'Метод Идкстжпег:: get_ReplicateX (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8855f819cb00d46297220c41deb6b81d6150e0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675984"
---
# <a name="idxtjpegget_replicatex-method"></a><span data-ttu-id="d9345-103">Метод Идкстжпег:: Get \_ репликатекс</span><span class="sxs-lookup"><span data-stu-id="d9345-103">IDxtJpeg::get\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="d9345-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d9345-104">\[Deprecated.</span></span> <span data-ttu-id="d9345-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9345-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9345-106">`get_ReplicateX`Метод извлекает количество раз, когда шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d9345-106">The `get_ReplicateX` method retrieves the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9345-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9345-107">Syntax</span></span>


```C++
HRESULT get_ReplicateX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d9345-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9345-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9345-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d9345-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d9345-110">Получает количество раз, когда шаблон очистки реплицируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="d9345-110">Receives the number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9345-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9345-111">Return value</span></span>

<span data-ttu-id="d9345-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d9345-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9345-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9345-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9345-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9345-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9345-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="d9345-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d9345-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d9345-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d9345-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d9345-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9345-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d9345-118">Requirements</span></span>



| <span data-ttu-id="d9345-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d9345-119">Requirement</span></span> | <span data-ttu-id="d9345-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d9345-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9345-121">Header</span><span class="sxs-lookup"><span data-stu-id="d9345-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d9345-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9345-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d9345-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9345-123">Library</span></span><br/> | <dl> <span data-ttu-id="d9345-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9345-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9345-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9345-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9345-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="d9345-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




