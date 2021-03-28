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
# <a name="waveprefixcountbits-function"></a>Функция Вавепрефикскаунтбитс

Возвращает сумму всех заданных переменных типа Boolean, для которых задано значение true для всех активных дорожек с индексами, меньшими, чем текущая полоса.

## <a name="syntax"></a>Синтаксис


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ббит* 
</dt> <dd>

Указанные логические переменные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Сумма всех заданных переменных типа Boolean задается равным true во всех активных желобах с индексами, меньшими, чем текущая полоса.

## <a name="remarks"></a>Примечания

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

В следующем коде показано, как реализовать сжатую запись в упорядоченный поток, в котором количество элементов, записываемых в каждую полосу, равно 1 или 0.

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

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 




