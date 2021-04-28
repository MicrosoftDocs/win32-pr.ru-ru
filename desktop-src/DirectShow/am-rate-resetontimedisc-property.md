---
description: AM_RATE_ResetOnTimeDisc свойство — применяется к Windows Vista и более поздним версиям.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Свойство AM_RATE_ResetOnTimeDisc (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096612"
---
# <a name="am_rate_resetontimedisc-property"></a>\_ \_ Свойство ресетонтимедиск Rate

Применяется к Windows Vista и более поздним версиям.

Это свойство запрашивает, будет ли декодер повторно синхронизировать метки времени вывода со штампами времени ввода, когда декодер получает пример с флагом небесперебойности.

Это свойство доступно для чтения и записи.



| Метка | Значение |
|-------------------|-------------------------------|
| Идентификатор GUID набора свойств | \_Кспропсетид \_ тсратечанже |
| Идентификатор свойства       | \_Ставка \_ ресетонтимедиск     |
| Тип данных         | **DWORD**                     |



 

## <a name="remarks"></a>Remarks

Это свойство поддерживает плавные изменения скорости. Если значение этого свойства равно **true** и декодер получает образец входных данных с \_ \_ флагом тимедисконтинуити, декодированный кадр должен иметь ту же метку времени, что и входной фрейм.

Чтобы получить \_ пример \_ флага тимедисконтинуити, вызовите [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) в примере. Флаг задается в элементе **двсамплефлагс** структуры [**\_ \_ свойств SAMPLE2 AM**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

Дополнительные сведения см. [в статье улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Двдмедиа. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Набор свойств изменения скорости**](rate-change-property-set.md)
</dt> </dl>

 

 




