---
description: Метод получения \_ репликации извлекает количество раз, когда шаблон очистки реплицируется по вертикали.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'Метод Идкстжпег:: get_ReplicateY (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679972"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="fe8bb-103">Метод Идкстжпег:: Get \_ replicate</span><span class="sxs-lookup"><span data-stu-id="fe8bb-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="fe8bb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-104">\[Deprecated.</span></span> <span data-ttu-id="fe8bb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe8bb-106">`get_ReplicateY`Метод извлекает количество раз, когда шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8bb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe8bb-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fe8bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe8bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8bb-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-110">Получает количество раз, когда шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe8bb-111">Return value</span></span>

<span data-ttu-id="fe8bb-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe8bb-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8bb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe8bb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe8bb-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe8bb-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fe8bb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe8bb-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fe8bb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe8bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fe8bb-118">Requirements</span></span>



| <span data-ttu-id="fe8bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fe8bb-119">Requirement</span></span> | <span data-ttu-id="fe8bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fe8bb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8bb-121">Header</span><span class="sxs-lookup"><span data-stu-id="fe8bb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fe8bb-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8bb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe8bb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe8bb-123">Library</span></span><br/> | <dl> <span data-ttu-id="fe8bb-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe8bb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe8bb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe8bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8bb-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="fe8bb-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




