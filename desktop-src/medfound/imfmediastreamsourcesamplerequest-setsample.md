---
description: Задает образец для источника потока мультимедиа.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Метод Имфмедиастреамсаурцесамплерекуест:: Сетсампле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664817"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="d70bf-103">Метод Имфмедиастреамсаурцесамплерекуест:: Сетсампле</span><span class="sxs-lookup"><span data-stu-id="d70bf-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="d70bf-104">Задает образец для источника потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d70bf-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d70bf-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="d70bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d70bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70bf-107">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d70bf-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d70bf-108">Образец для источника потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d70bf-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70bf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d70bf-109">Return value</span></span>

<span data-ttu-id="d70bf-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d70bf-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d70bf-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d70bf-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70bf-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d70bf-112">Requirements</span></span>



| <span data-ttu-id="d70bf-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d70bf-113">Requirement</span></span> | <span data-ttu-id="d70bf-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d70bf-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d70bf-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d70bf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d70bf-116">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="d70bf-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d70bf-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d70bf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d70bf-118">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d70bf-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="d70bf-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d70bf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d70bf-120"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d70bf-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70bf-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d70bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70bf-122">**имфмедиастреамсаурцесамплерекуест**</span><span class="sxs-lookup"><span data-stu-id="d70bf-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




