---
description: Указывает максимальное количество выходных образцов, которые преMicrosoft Media Foundation преобразование MFT в любой момент времени будут ожидать в конвейере.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Атрибут MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a7d00fcb5a11d756ed4848e3e600a6fd1cca32203ff7234cb01963dfcb5149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663914"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>\_ \_ \_ \_ Атрибут счетчика выборки МИНИМАЛЬного значения SA \_ MF

Указывает максимальное количество выходных образцов, которые преMicrosoft Media Foundation преобразование MFT в любой момент времени будут ожидать в конвейере.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется только к МФТС, в котором для выделения собственных выходных образцов используется круглый буфер. Другие МФТС игнорируют этот атрибут.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы добавить атрибут.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




