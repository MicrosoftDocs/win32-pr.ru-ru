---
description: Метод постановки \_ репликации указывает, сколько раз шаблон очистки реплицируется по вертикали.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: 'Идкстжпег: метод ut_ReplicateY:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ac5016635cb8e6f5b81b99f1ea67f0282878d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675545"
---
# <a name="idxtjpegput_replicatey-method"></a><span data-ttu-id="f75f3-103">Идкстжпег: \_ метод репликации:p UT</span><span class="sxs-lookup"><span data-stu-id="f75f3-103">IDxtJpeg::put\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="f75f3-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f75f3-104">\[Deprecated.</span></span> <span data-ttu-id="f75f3-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f75f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f75f3-106">`put_ReplicateY`Метод указывает, сколько раз шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="f75f3-106">The `put_ReplicateY` method specifies the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="f75f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f75f3-107">Syntax</span></span>


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f75f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f75f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f75f3-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f75f3-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f75f3-110">Количество раз, когда шаблон очистки реплицируется по вертикали.</span><span class="sxs-lookup"><span data-stu-id="f75f3-110">The number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f75f3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f75f3-111">Return value</span></span>

<span data-ttu-id="f75f3-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f75f3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f75f3-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f75f3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f75f3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f75f3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f75f3-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f75f3-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f75f3-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f75f3-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f75f3-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f75f3-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f75f3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f75f3-118">Requirements</span></span>



| <span data-ttu-id="f75f3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f75f3-119">Requirement</span></span> | <span data-ttu-id="f75f3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f75f3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f75f3-121">Header</span><span class="sxs-lookup"><span data-stu-id="f75f3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f75f3-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f75f3-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f75f3-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f75f3-123">Library</span></span><br/> | <dl> <span data-ttu-id="f75f3-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f75f3-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f75f3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f75f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75f3-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="f75f3-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




