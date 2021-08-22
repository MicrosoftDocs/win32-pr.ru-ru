---
description: Указывает максимальный поддерживаемый кодировщиком обработчик запросов.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Свойство CODECAPI_AVEncVideoMaxQP (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606324"
---
# <a name="codecapi_avencvideomaxqp-property"></a>КОДЕКАПИ \_ авенквидеомакскп, свойство

Указывает максимальный поддерживаемый кодировщиком обработчик запросов.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеомакскп**

## <a name="remarks"></a>Remarks

**Кодировщики H. 264/AVC:**

Кодировщик должен поддерживать [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранже**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Это статическое свойство означает, что его можно задать только до начала сеанса кодирования.

Значение по умолчанию должно быть максимальным числом запросов QP, разрешенным соответствующим стандартом кодирования. Например, кодировщики H. 264 должны иметь значение по умолчанию 51.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[КОДЕКАПИ \_ авенквидеоминкп](codecapi-avencvideominqp.md)
</dt> </dl>

 

