---
title: Свойство IMsRdpCameraRedirConfigCollection EncodingQuality
description: Задает качество кодирования (скорость потока).
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енкодингкуалити
- Службы удаленных рабочих столов свойства Енкодингкуалити, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Енкодингкуалити
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494157"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="38d11-106">Свойство Имсрдпкамераредирконфигколлектион:: Енкодингкуалити</span><span class="sxs-lookup"><span data-stu-id="38d11-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="38d11-107">Задает качество кодирования (скорость потока).</span><span class="sxs-lookup"><span data-stu-id="38d11-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="38d11-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="38d11-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d11-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38d11-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="38d11-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="38d11-110">Property value</span></span>

<span data-ttu-id="38d11-111">Одно из следующих значений перечисления **камераредиренкодингкуалити** , определяющее качество кодирования (скорость потока).</span><span class="sxs-lookup"><span data-stu-id="38d11-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="38d11-112">Имя элемента перечисления</span><span class="sxs-lookup"><span data-stu-id="38d11-112">Enum member name</span></span> | <span data-ttu-id="38d11-113">Значение</span><span class="sxs-lookup"><span data-stu-id="38d11-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="38d11-114">енкодингкуалитилов</span><span class="sxs-lookup"><span data-stu-id="38d11-114">encodingQualityLow</span></span> | <span data-ttu-id="38d11-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="38d11-115">0x0000</span></span> |
| <span data-ttu-id="38d11-116">енкодингкуалитимедиум</span><span class="sxs-lookup"><span data-stu-id="38d11-116">encodingQualityMedium</span></span> | <span data-ttu-id="38d11-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="38d11-117">0x0001</span></span> |
| <span data-ttu-id="38d11-118">енкодингкуалитихигх</span><span class="sxs-lookup"><span data-stu-id="38d11-118">encodingQualityHigh</span></span> | <span data-ttu-id="38d11-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="38d11-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="38d11-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38d11-120">Requirements</span></span>

| <span data-ttu-id="38d11-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38d11-121">Requirement</span></span> | <span data-ttu-id="38d11-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38d11-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="38d11-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38d11-123">Minimum supported client</span></span>| <span data-ttu-id="38d11-124">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="38d11-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="38d11-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="38d11-125">Type library</span></span>            | <span data-ttu-id="38d11-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="38d11-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="38d11-127">DLL</span><span class="sxs-lookup"><span data-stu-id="38d11-127">DLL</span></span>                  | <span data-ttu-id="38d11-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="38d11-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="38d11-129">IID</span><span class="sxs-lookup"><span data-stu-id="38d11-129">IID</span></span>                      | <span data-ttu-id="38d11-130">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="38d11-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="38d11-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38d11-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d11-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="38d11-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>