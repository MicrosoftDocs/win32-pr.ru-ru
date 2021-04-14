---
description: Указывает матрицу канала, которая используется для преобразования исходных каналов в каналы назначения (например, для преобразования 5,1 в стерео).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Свойство MFPKEY_WMRESAMP_CHANNELMTX (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692797"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="ebc99-103">МФПКЭЙ \_ вмресамп \_ Чаннелмткс, свойство</span><span class="sxs-lookup"><span data-stu-id="ebc99-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="ebc99-104">Указывает матрицу канала, которая используется для преобразования исходных каналов в каналы назначения (например, для преобразования 5,1 в стерео).</span><span class="sxs-lookup"><span data-stu-id="ebc99-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ebc99-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="ebc99-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ebc99-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ebc99-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ebc99-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ebc99-107">Data Type</span></span>

<span data-ttu-id="ebc99-108">VT \_ I4 \| , \_ массив VT</span><span class="sxs-lookup"><span data-stu-id="ebc99-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="ebc99-109">Применение</span><span class="sxs-lookup"><span data-stu-id="ebc99-109">Applies To</span></span>

-   [<span data-ttu-id="ebc99-110">DSP по интерполяции аудио</span><span class="sxs-lookup"><span data-stu-id="ebc99-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="ebc99-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ebc99-111">Remarks</span></span>

<span data-ttu-id="ebc99-112">Значение свойства является матрицей коэффициентов NS x ND, где NS — число исходных каналов, а ND — количество целевых каналов.</span><span class="sxs-lookup"><span data-stu-id="ebc99-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="ebc99-113">Коэффициенты задаются в децибел с помощью следующей формулы:</span><span class="sxs-lookup"><span data-stu-id="ebc99-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="ebc99-114">int (65536 \* 20 \* LOG10 (DB))</span><span class="sxs-lookup"><span data-stu-id="ebc99-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="ebc99-115">Матрица хранится в виде массива в основном порядке строк, где номер строки является исходным каналом, а номер столбца — целевым каналом.</span><span class="sxs-lookup"><span data-stu-id="ebc99-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="ebc99-116">Таким образом, если матрица имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="ebc99-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="ebc99-117">Затем следует указать массив следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ebc99-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="ebc99-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ebc99-118">Requirements</span></span>



| <span data-ttu-id="ebc99-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ebc99-119">Requirement</span></span> | <span data-ttu-id="ebc99-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ebc99-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc99-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebc99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc99-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebc99-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebc99-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebc99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc99-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebc99-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebc99-125">Header</span><span class="sxs-lookup"><span data-stu-id="ebc99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebc99-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc99-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc99-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebc99-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc99-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebc99-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
