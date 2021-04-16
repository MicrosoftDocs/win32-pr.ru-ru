---
description: Метод Get \_ стреамленгс извлекает длительность текущего потока.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'Метод Имедиадет:: get_StreamLength (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679709"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="ef1db-103">Метод Имедиадет:: Get \_ стреамленгс</span><span class="sxs-lookup"><span data-stu-id="ef1db-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="ef1db-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ef1db-104">\[Deprecated.</span></span> <span data-ttu-id="ef1db-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef1db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef1db-106">`get_StreamLength`Метод получает длительность текущего потока.</span><span class="sxs-lookup"><span data-stu-id="ef1db-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef1db-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ef1db-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef1db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1db-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ef1db-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1db-110">Получает длительность потока в секундах.</span><span class="sxs-lookup"><span data-stu-id="ef1db-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1db-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef1db-111">Return value</span></span>

<span data-ttu-id="ef1db-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ef1db-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef1db-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef1db-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1db-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef1db-114">Remarks</span></span>

<span data-ttu-id="ef1db-115">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="ef1db-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="ef1db-116">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ef1db-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="ef1db-117">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="ef1db-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef1db-118">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ef1db-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef1db-119">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef1db-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef1db-120">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ef1db-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef1db-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ef1db-121">Requirements</span></span>



| <span data-ttu-id="ef1db-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ef1db-122">Requirement</span></span> | <span data-ttu-id="ef1db-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1db-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1db-124">Header</span><span class="sxs-lookup"><span data-stu-id="ef1db-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ef1db-125"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1db-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef1db-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef1db-126">Library</span></span><br/> | <dl> <span data-ttu-id="ef1db-127"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef1db-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1db-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef1db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1db-129">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="ef1db-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="ef1db-130">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ef1db-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




