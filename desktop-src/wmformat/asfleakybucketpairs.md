---
title: асфлеакибуккетпаирс
description: Атрибут Асфлеакибуккетпаирс является необязательным атрибутом, который описывает требования к буферизации для файла переменной скорости.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Формат Windows Media Асфлеакибуккетпаирс
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691414"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="dceb0-104">асфлеакибуккетпаирс</span><span class="sxs-lookup"><span data-stu-id="dceb0-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="dceb0-105">Атрибут **асфлеакибуккетпаирс** является необязательным атрибутом, который описывает требования к буферизации для файла переменной скорости.</span><span class="sxs-lookup"><span data-stu-id="dceb0-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="dceb0-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="dceb0-106">Global Constant</span></span>

<span data-ttu-id="dceb0-107">g \_ всзасфлеакибуккетпаирс</span><span class="sxs-lookup"><span data-stu-id="dceb0-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="dceb0-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dceb0-108">Data Type</span></span>

<span data-ttu-id="dceb0-109">**\_ \_ двоичный тип ВМТ**</span><span class="sxs-lookup"><span data-stu-id="dceb0-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="dceb0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dceb0-110">Remarks</span></span>

<span data-ttu-id="dceb0-111">Этот атрибут имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="dceb0-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="dceb0-112">Где *вресервед* должно равняться нулю, а *контейнер* — массив [**\_ \_ \_ пар сегментов с утечкой**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) данных типа WM.</span><span class="sxs-lookup"><span data-stu-id="dceb0-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="dceb0-113">Массив должен содержать по крайней мере две записи, но может быть больше.</span><span class="sxs-lookup"><span data-stu-id="dceb0-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="dceb0-114">Объект "читатель" использует этот атрибут для определения объема содержимого для буферизации перед воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="dceb0-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="dceb0-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dceb0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dceb0-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="dceb0-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




