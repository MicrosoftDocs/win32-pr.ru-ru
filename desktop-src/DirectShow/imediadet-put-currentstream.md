---
description: Метод размещения \_ куррентстреам указывает номер потока для использования средством обнаружения мультимедиа.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'Имедиадет: метод ut_CurrentStream:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675440"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="31583-103">Имедиадет::p UT \_ куррентстреам метод</span><span class="sxs-lookup"><span data-stu-id="31583-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="31583-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="31583-104">\[Deprecated.</span></span> <span data-ttu-id="31583-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="31583-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="31583-106">`put_CurrentStream`Метод задает номер потока для использования средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31583-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="31583-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31583-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="31583-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31583-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31583-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31583-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31583-110">Номер потока.</span><span class="sxs-lookup"><span data-stu-id="31583-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31583-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31583-111">Return value</span></span>

<span data-ttu-id="31583-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="31583-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31583-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31583-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31583-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31583-114">Remarks</span></span>

<span data-ttu-id="31583-115">Перед вызовом этого метода вызовите [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) , чтобы задать имя файла.</span><span class="sxs-lookup"><span data-stu-id="31583-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="31583-116">Вызовите метод [**имедиадет:: Get \_ аутпутстреамс**](imediadet-get-outputstreams.md) , чтобы определить количество потоков, содержащихся в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="31583-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="31583-117">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="31583-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="31583-118">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="31583-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="31583-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="31583-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="31583-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="31583-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="31583-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="31583-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31583-122">Требования</span><span class="sxs-lookup"><span data-stu-id="31583-122">Requirements</span></span>



| <span data-ttu-id="31583-123">Требование</span><span class="sxs-lookup"><span data-stu-id="31583-123">Requirement</span></span> | <span data-ttu-id="31583-124">Значение</span><span class="sxs-lookup"><span data-stu-id="31583-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31583-125">Header</span><span class="sxs-lookup"><span data-stu-id="31583-125">Header</span></span><br/>  | <dl> <span data-ttu-id="31583-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="31583-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="31583-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31583-127">Library</span></span><br/> | <dl> <span data-ttu-id="31583-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31583-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31583-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31583-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31583-130">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="31583-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="31583-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="31583-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




