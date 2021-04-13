---
description: Указывает минимальное количество последовательных выборок, которые Microsoft Media Foundation преобразование (MFT) должны допускать аустандинг в любое заданное время.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Атрибут MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265356"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>\_ \_ \_ Последовательное значение \_ \_ счетчика минимального количества выходных данных SA \_ MF

Указывает минимальное количество последовательных выборок, которые Microsoft Media Foundation преобразование (MFT) должны допускать аустандинг в любое заданное время.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется только к МФТС, в котором для выделения собственных выходных образцов используется круглый буфер. Другие МФТС игнорируют этот атрибут.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы добавить атрибут.

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

 

 




