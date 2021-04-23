---
description: Метод ApplyChanges применяет все измененные свойства.
ms.assetid: dece1e61-7fe1-40f1-8d1d-89b5a334d04e
title: 'Метод Идкстжпег:: ApplyChanges (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.ApplyChanges
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 522df2fc362b0332d4eb41e9a2f10201bfcdec9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675180"
---
# <a name="idxtjpegapplychanges-method"></a><span data-ttu-id="796f3-103">Метод Идкстжпег:: ApplyChanges</span><span class="sxs-lookup"><span data-stu-id="796f3-103">IDxtJpeg::ApplyChanges method</span></span>

> [!Note]  
> <span data-ttu-id="796f3-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="796f3-104">\[Deprecated.</span></span> <span data-ttu-id="796f3-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="796f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="796f3-106">`ApplyChanges`Метод применяет все измененные свойства.</span><span class="sxs-lookup"><span data-stu-id="796f3-106">The `ApplyChanges` method applies any properties that have changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="796f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="796f3-107">Syntax</span></span>


```C++
HRESULT ApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="796f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="796f3-108">Parameters</span></span>

<span data-ttu-id="796f3-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="796f3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="796f3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="796f3-110">Return value</span></span>

<span data-ttu-id="796f3-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="796f3-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="796f3-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="796f3-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="796f3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="796f3-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="796f3-114">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="796f3-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="796f3-115">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="796f3-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="796f3-116">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="796f3-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="796f3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="796f3-117">Requirements</span></span>



| <span data-ttu-id="796f3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="796f3-118">Requirement</span></span> | <span data-ttu-id="796f3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="796f3-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="796f3-120">Header</span><span class="sxs-lookup"><span data-stu-id="796f3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="796f3-121"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="796f3-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="796f3-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="796f3-122">Library</span></span><br/> | <dl> <span data-ttu-id="796f3-123"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="796f3-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="796f3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="796f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="796f3-125">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="796f3-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




