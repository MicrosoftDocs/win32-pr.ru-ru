---
description: Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Свойство CODECAPI_AVEncVideoMaxNumRefFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157007"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>КОДЕКАПИ \_ авенквидеомакснумреффраме, свойство

Указывает максимальное число кадров ссылок, поддерживаемое кодировщиком.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеомакснумреффраме**

## <a name="remarks"></a>Комментарии

Для H. 264 это соответствует параметру последовательности Set **Max \_ NUM \_ ref \_ frames** , как определено в спецификации H. 264.

**Кодировщики H. 264/AVC:**

Кодировщики могут использовать меньше кадров ссылок для того, чтобы соблюдать уровень, указанный в битовый поток.

Кодировщики должны поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранжее**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Это статическое свойство означает, что его можно задать только до начала сеанса кодирования.

Рекомендуемое значение по умолчанию — 2.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

