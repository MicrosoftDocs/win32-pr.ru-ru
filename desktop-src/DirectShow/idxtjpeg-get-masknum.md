---
description: Метод Get \_ маскнум извлекает код очистки SMPTE.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Метод Идкстжпег:: get_MaskNum (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675286"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="f158a-103">Метод Идкстжпег:: Get \_ маскнум</span><span class="sxs-lookup"><span data-stu-id="f158a-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="f158a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f158a-104">\[Deprecated.</span></span> <span data-ttu-id="f158a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f158a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f158a-106">`get_MaskNum`Метод извлекает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f158a-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="f158a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f158a-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f158a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f158a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f158a-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f158a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f158a-110">Получает код очистки SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f158a-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="f158a-111">Список поддерживаемых SMPTE очистки см. в разделе Переход на [SMPTE очистки](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="f158a-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f158a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f158a-112">Return value</span></span>

<span data-ttu-id="f158a-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f158a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f158a-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f158a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f158a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f158a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f158a-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f158a-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f158a-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f158a-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f158a-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f158a-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f158a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f158a-119">Requirements</span></span>



| <span data-ttu-id="f158a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f158a-120">Requirement</span></span> | <span data-ttu-id="f158a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f158a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f158a-122">Header</span><span class="sxs-lookup"><span data-stu-id="f158a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f158a-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f158a-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f158a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f158a-124">Library</span></span><br/> | <dl> <span data-ttu-id="f158a-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f158a-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f158a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f158a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f158a-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="f158a-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




