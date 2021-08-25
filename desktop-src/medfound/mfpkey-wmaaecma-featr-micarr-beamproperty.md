---
description: Указывает, какой образ используется для записи голоса, используемой DSP для обработки массива микрофона.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Свойство MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9a91cef7d270af37adc8fda9805d7bf275ef9877883ed8ff8cfdbf9e7a55e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953534"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ микарр, \_ свойство

Указывает, какой образ используется для записи голоса, используемой DSP для обработки массива микрофона.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

Задайте это свойство, если свойство [мфпкэй \_ вмааекма \_ феатр \_ \_ mode микарр](mfpkey-wmaaecma-featr-micarr-modeproperty.md) имеет значение микаррай \_ extern \_ .

Если значение [**мфпкэй \_ вмааекма \_ феатр \_ микарр \_ mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) равно микаррай Single- \_ \_ лучевой, можно прочитать это свойство, чтобы запросить, какую форму он выбрал в DSP.

Это свойство может иметь следующие значения. Значения находятся в градусах по горизонтали.



| Значение | Описание              |
|-------|--------------------------|
| 0     | -50 градусов.             |
| 1     | -40 градусов.             |
| 2     | – 30 градусов.             |
| 3     | -20 градусов.             |
| 4     | -10 градусов.             |
| 5     | 0 градусов (Центральная наобразная). |
| 6     | 10 градусов.              |
| 7     | 20 градусов.              |
| 8     | 30 градусов.              |
| 9     | 40 градусов.              |
| 10    | 50 градусов.              |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
