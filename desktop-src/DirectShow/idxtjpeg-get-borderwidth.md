---
description: Метод Get \_ BorderWidth получает ширину сплошной границы вдоль краев шаблона очистки.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'Метод Идкстжпег:: get_BorderWidth (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28405c08d5666c8f182e0ffdb6ed1aa7bac599d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675986"
---
# <a name="idxtjpegget_borderwidth-method"></a><span data-ttu-id="e79cb-103">Метод Идкстжпег:: Get \_ BorderWidth</span><span class="sxs-lookup"><span data-stu-id="e79cb-103">IDxtJpeg::get\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="e79cb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e79cb-104">\[Deprecated.</span></span> <span data-ttu-id="e79cb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e79cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e79cb-106">`get_BorderWidth`Метод получает ширину сплошной границы вдоль краев шаблона очистки.</span><span class="sxs-lookup"><span data-stu-id="e79cb-106">The `get_BorderWidth` method retrieves the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="e79cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e79cb-107">Syntax</span></span>


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e79cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e79cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e79cb-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e79cb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e79cb-110">Получает ширину границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e79cb-110">Receives the width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e79cb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e79cb-111">Return value</span></span>

<span data-ttu-id="e79cb-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e79cb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e79cb-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e79cb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e79cb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e79cb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e79cb-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e79cb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e79cb-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e79cb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e79cb-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e79cb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e79cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e79cb-118">Requirements</span></span>



| <span data-ttu-id="e79cb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e79cb-119">Requirement</span></span> | <span data-ttu-id="e79cb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e79cb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e79cb-121">Header</span><span class="sxs-lookup"><span data-stu-id="e79cb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e79cb-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e79cb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e79cb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e79cb-123">Library</span></span><br/> | <dl> <span data-ttu-id="e79cb-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e79cb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e79cb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e79cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e79cb-126">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="e79cb-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




