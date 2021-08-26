---
description: Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Атрибут MF_ENABLE_3DVIDEO_OUTPUT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013174"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>\_Включить \_ \_ выходной атрибут 3DVIDEO MF

Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение атрибута является членом перечисления [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Этот атрибут применяется только в том случае, если MFT возвращает **значение true** для атрибута [ \_ \_ 3DVIDEO поддержки MFT](mft-support-3dvideo.md) .

Чтобы получить или задать этот атрибут, необходимо вызвать [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




