---
description: '\_Метод маскнаме указывает имя JPEG-файла, используемого в качестве маски очистки.'
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'Идкстжпег: метод ut_MaskName:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675750"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="3be55-103">Идкстжпег::p UT \_ маскнаме метод</span><span class="sxs-lookup"><span data-stu-id="3be55-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="3be55-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3be55-104">\[Deprecated.</span></span> <span data-ttu-id="3be55-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3be55-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3be55-106">`put_MaskName`Метод задает имя JPEG-файла, используемого в качестве маски очистки.</span><span class="sxs-lookup"><span data-stu-id="3be55-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="3be55-107">Эта маска будет использоваться вместо одной из встроенных масок очистки.</span><span class="sxs-lookup"><span data-stu-id="3be55-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="3be55-108">Файл должен содержать монохромный градиент с 8 битами на пиксель.</span><span class="sxs-lookup"><span data-stu-id="3be55-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="3be55-109">Градиент используется в качестве маски для определения хода выполнения очистки.</span><span class="sxs-lookup"><span data-stu-id="3be55-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be55-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3be55-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3be55-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3be55-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be55-112">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3be55-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be55-113">Указывает имя файла.</span><span class="sxs-lookup"><span data-stu-id="3be55-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be55-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3be55-114">Return value</span></span>

<span data-ttu-id="3be55-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3be55-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3be55-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3be55-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be55-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3be55-117">Remarks</span></span>

<span data-ttu-id="3be55-118">Чтобы вернуться к встроенной маске, установите свойство **маскнум** .</span><span class="sxs-lookup"><span data-stu-id="3be55-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="3be55-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="3be55-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3be55-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3be55-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3be55-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3be55-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3be55-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3be55-122">Requirements</span></span>



| <span data-ttu-id="3be55-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3be55-123">Requirement</span></span> | <span data-ttu-id="3be55-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3be55-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3be55-125">Header</span><span class="sxs-lookup"><span data-stu-id="3be55-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3be55-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be55-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3be55-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3be55-127">Library</span></span><br/> | <dl> <span data-ttu-id="3be55-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3be55-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be55-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3be55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be55-130">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="3be55-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="3be55-131">**Идкстжпег::p UT \_ маскнум**</span><span class="sxs-lookup"><span data-stu-id="3be55-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




