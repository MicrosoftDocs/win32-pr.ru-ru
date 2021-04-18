---
description: Метод получения \_ смещения извлекает вертикальное смещение источника очистки.
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'Метод Идкстжпег:: get_OffsetY (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675285"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="18928-103">Метод СМЕЩ Идкстжпег:: Get \_</span><span class="sxs-lookup"><span data-stu-id="18928-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="18928-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="18928-104">\[Deprecated.</span></span> <span data-ttu-id="18928-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18928-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="18928-106">`get_OffsetY`Метод получает вертикальное смещение источника очистки.</span><span class="sxs-lookup"><span data-stu-id="18928-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="18928-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18928-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="18928-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18928-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18928-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="18928-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="18928-110">Получает вертикальное смещение начала очистки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="18928-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="18928-111">Центр очистки смещается на этот объем.</span><span class="sxs-lookup"><span data-stu-id="18928-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18928-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18928-112">Return value</span></span>

<span data-ttu-id="18928-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="18928-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18928-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18928-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18928-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18928-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18928-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="18928-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="18928-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="18928-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="18928-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="18928-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18928-119">Требования</span><span class="sxs-lookup"><span data-stu-id="18928-119">Requirements</span></span>



| <span data-ttu-id="18928-120">Требование</span><span class="sxs-lookup"><span data-stu-id="18928-120">Requirement</span></span> | <span data-ttu-id="18928-121">Значение</span><span class="sxs-lookup"><span data-stu-id="18928-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18928-122">Header</span><span class="sxs-lookup"><span data-stu-id="18928-122">Header</span></span><br/>  | <dl> <span data-ttu-id="18928-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="18928-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="18928-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18928-124">Library</span></span><br/> | <dl> <span data-ttu-id="18928-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18928-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18928-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18928-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18928-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="18928-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




