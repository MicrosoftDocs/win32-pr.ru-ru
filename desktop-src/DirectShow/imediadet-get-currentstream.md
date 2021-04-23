---
description: Метод Get \_ куррентстреам извлекает номер потока, который в настоящее время используется средством обнаружения мультимедиа.
ms.assetid: 0f590498-e639-4b6b-be1d-f1e4a36282cb
title: 'Метод Имедиадет:: get_CurrentStream (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e664e88862a6bc124a88ac23cedf29e687d51e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675543"
---
# <a name="imediadetget_currentstream-method"></a><span data-ttu-id="0f533-103">Метод Имедиадет:: Get \_ куррентстреам</span><span class="sxs-lookup"><span data-stu-id="0f533-103">IMediaDet::get\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="0f533-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0f533-104">\[Deprecated.</span></span> <span data-ttu-id="0f533-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f533-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f533-106">`get_CurrentStream`Метод получает номер потока, который в настоящее время используется средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0f533-106">The `get_CurrentStream` method retrieves the stream number currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f533-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f533-107">Syntax</span></span>


```C++
HRESULT get_CurrentStream(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0f533-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f533-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f533-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f533-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f533-110">Получает текущий номер потока.</span><span class="sxs-lookup"><span data-stu-id="0f533-110">Receives the current stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f533-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f533-111">Return value</span></span>

<span data-ttu-id="0f533-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0f533-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f533-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f533-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f533-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f533-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f533-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0f533-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f533-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f533-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f533-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0f533-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f533-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0f533-118">Requirements</span></span>



| <span data-ttu-id="0f533-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0f533-119">Requirement</span></span> | <span data-ttu-id="0f533-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0f533-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f533-121">Header</span><span class="sxs-lookup"><span data-stu-id="0f533-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0f533-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f533-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f533-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f533-123">Library</span></span><br/> | <dl> <span data-ttu-id="0f533-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f533-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f533-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f533-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f533-126">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="0f533-126">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="0f533-127">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0f533-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




