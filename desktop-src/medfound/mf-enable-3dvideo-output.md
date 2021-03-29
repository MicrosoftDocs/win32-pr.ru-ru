---
description: Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Атрибут MF_ENABLE_3DVIDEO_OUTPUT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898358"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>\_Включить \_ \_ выходной атрибут 3DVIDEO MF

Указывает, как преобразование Media Foundation (MFT) должно выводить поток трехмерного стереоскопик видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение атрибута является членом перечисления [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Этот атрибут применяется только в том случае, если MFT возвращает **значение true** для атрибута [ \_ \_ 3DVIDEO поддержки MFT](mft-support-3dvideo.md) .

Чтобы получить или задать этот атрибут, необходимо вызвать [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




