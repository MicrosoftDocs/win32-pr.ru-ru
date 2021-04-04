---
title: Свойство IMsRdpCameraRedirConfigCollection EncodeVideo
description: Указывает, является ли поток видео закодированным H. 264.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енкодевидео
- Службы удаленных рабочих столов свойства Енкодевидео, интерфейс Имсрдпкамераредирконфигколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпкамераредирконфигколлектион, свойство Енкодевидео
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139178"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="b5ffb-106">Свойство Имсрдпкамераредирконфигколлектион:: Енкодевидео</span><span class="sxs-lookup"><span data-stu-id="b5ffb-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="b5ffb-107">Указывает, является ли поток видео закодированным H. 264.</span><span class="sxs-lookup"><span data-stu-id="b5ffb-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="b5ffb-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b5ffb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ffb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5ffb-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="b5ffb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b5ffb-110">Property value</span></span>

<span data-ttu-id="b5ffb-111">Значение, указывающее, является ли поток видео закодированным H. 264.</span><span class="sxs-lookup"><span data-stu-id="b5ffb-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ffb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ffb-112">Requirements</span></span>

| <span data-ttu-id="b5ffb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ffb-113">Requirement</span></span> | <span data-ttu-id="b5ffb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ffb-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b5ffb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5ffb-115">Minimum supported client</span></span>| <span data-ttu-id="b5ffb-116">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="b5ffb-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="b5ffb-117">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b5ffb-117">Type library</span></span>            | <span data-ttu-id="b5ffb-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b5ffb-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b5ffb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ffb-119">DLL</span></span>                  | <span data-ttu-id="b5ffb-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b5ffb-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b5ffb-121">IID</span><span class="sxs-lookup"><span data-stu-id="b5ffb-121">IID</span></span>                      | <span data-ttu-id="b5ffb-122">IID \_ имсрдпкамераредирконфигколлектион определен как AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="b5ffb-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="b5ffb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5ffb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ffb-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="b5ffb-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>