---
description: Метод "получить \_ Масштаб" извлекает величину, на которую производится растяжение очистки по вертикали.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: 'Метод Идкстжпег:: get_ScaleY (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4ca3feb0177ad1c9172721ca312e810fdb105b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675983"
---
# <a name="idxtjpegget_scaley-method"></a><span data-ttu-id="689fa-103">Идкстжпег:: Get \_ метод масштабирования</span><span class="sxs-lookup"><span data-stu-id="689fa-103">IDxtJpeg::get\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="689fa-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="689fa-104">\[Deprecated.</span></span> <span data-ttu-id="689fa-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="689fa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="689fa-106">`get_ScaleY`Метод получает величину, на которую производится растяжение очистки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="689fa-106">The `get_ScaleY` method retrieves the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="689fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="689fa-107">Syntax</span></span>


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="689fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="689fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689fa-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="689fa-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="689fa-110">Получает величину, на которую производится растяжение очистки по вертикали в процентах от исходного определения очистки.</span><span class="sxs-lookup"><span data-stu-id="689fa-110">Receives the amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="689fa-111">Например, значение 1,0 означает отсутствие растяжения, а 2,0 означает 200% растяжения.</span><span class="sxs-lookup"><span data-stu-id="689fa-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689fa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="689fa-112">Return value</span></span>

<span data-ttu-id="689fa-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="689fa-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="689fa-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="689fa-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="689fa-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="689fa-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="689fa-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="689fa-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="689fa-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="689fa-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="689fa-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="689fa-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="689fa-119">Требования</span><span class="sxs-lookup"><span data-stu-id="689fa-119">Requirements</span></span>



| <span data-ttu-id="689fa-120">Требование</span><span class="sxs-lookup"><span data-stu-id="689fa-120">Requirement</span></span> | <span data-ttu-id="689fa-121">Значение</span><span class="sxs-lookup"><span data-stu-id="689fa-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="689fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="689fa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="689fa-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="689fa-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="689fa-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="689fa-124">Library</span></span><br/> | <dl> <span data-ttu-id="689fa-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="689fa-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="689fa-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="689fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689fa-127">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="689fa-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




