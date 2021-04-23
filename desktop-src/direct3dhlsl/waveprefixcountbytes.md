---
title: Функция Вавепрефикскаунтбитс
description: Возвращает сумму всех заданных переменных типа Boolean, для которых задано значение true для всех активных дорожек с индексами, меньшими, чем текущая полоса.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Функция Вавепрефикскаунтбитс HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070859"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="a38bd-104">Функция Вавепрефикскаунтбитс</span><span class="sxs-lookup"><span data-stu-id="a38bd-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="a38bd-105">Возвращает сумму всех заданных переменных типа Boolean, для которых задано значение true для всех активных дорожек с индексами, меньшими, чем текущая полоса.</span><span class="sxs-lookup"><span data-stu-id="a38bd-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38bd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a38bd-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="a38bd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a38bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38bd-108">*ббит*</span><span class="sxs-lookup"><span data-stu-id="a38bd-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="a38bd-109">Указанные логические переменные.</span><span class="sxs-lookup"><span data-stu-id="a38bd-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38bd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a38bd-110">Return value</span></span>

<span data-ttu-id="a38bd-111">Сумма всех заданных переменных типа Boolean задается равным true во всех активных желобах с индексами, меньшими, чем текущая полоса.</span><span class="sxs-lookup"><span data-stu-id="a38bd-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38bd-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a38bd-112">Remarks</span></span>

<span data-ttu-id="a38bd-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="a38bd-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="a38bd-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="a38bd-114">Examples</span></span>

<span data-ttu-id="a38bd-115">В следующем коде показано, как реализовать сжатую запись в упорядоченный поток, в котором количество элементов, записываемых в каждую полосу, равно 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="a38bd-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="a38bd-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a38bd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38bd-117">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="a38bd-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a38bd-118">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="a38bd-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




