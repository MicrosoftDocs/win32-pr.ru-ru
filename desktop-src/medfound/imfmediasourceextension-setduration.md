---
description: Задает продолжительность источника мультимедиа в 100-наносекундных единицах.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Метод Имфмедиасаурцеекстенсион:: Сетдуратион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693863"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="725f2-103">Метод Имфмедиасаурцеекстенсион:: Сетдуратион</span><span class="sxs-lookup"><span data-stu-id="725f2-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="725f2-104">Задает продолжительность источника мультимедиа в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="725f2-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="725f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="725f2-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="725f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="725f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725f2-107">*Длительность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="725f2-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="725f2-108">Длительность источника мультимедиа в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="725f2-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725f2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="725f2-109">Return value</span></span>

<span data-ttu-id="725f2-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="725f2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="725f2-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="725f2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="725f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="725f2-112">Requirements</span></span>



| <span data-ttu-id="725f2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="725f2-113">Requirement</span></span> | <span data-ttu-id="725f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="725f2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="725f2-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="725f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="725f2-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="725f2-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="725f2-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="725f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="725f2-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="725f2-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="725f2-119">IDL</span><span class="sxs-lookup"><span data-stu-id="725f2-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="725f2-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="725f2-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725f2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="725f2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725f2-122">**имфмедиасаурцеекстенсион**</span><span class="sxs-lookup"><span data-stu-id="725f2-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




