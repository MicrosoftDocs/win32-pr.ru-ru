---
description: Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Свойство CODECAPI_AVEncVideoMaxNumRefFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606424"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>КОДЕКАПИ \_ авенквидеомакснумреффраме, свойство

Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеомакснумреффраме**

## <a name="remarks"></a>Remarks

Для H. 264 это соответствует параметру последовательности Set **Max \_ NUM \_ ref \_ frames** , как определено в спецификации H. 264.

**Кодировщики H. 264/AVC:**

Кодировщики могут использовать меньше кадров ссылок для того, чтобы соблюдать уровень, указанный в битовый поток.

Кодировщики должны поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранжее**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Это статическое свойство означает, что его можно задать только до начала сеанса кодирования.

Рекомендуемое значение по умолчанию — 2.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

