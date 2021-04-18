---
description: Отключает использование преобразований Media Foundation на основе оборудования (МФТС) в подсистеме записи.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Атрибут MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711559"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>\_Атрибут MF \_ \_ Отключить \_ аппаратные \_ преобразования для ядра записи

Отключает использование преобразований Media Foundation на основе оборудования (МФТС) в подсистеме записи.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

По умолчанию подсистема отслеживания использует аппаратные декодеры или кодировщики. Чтобы отключить использование оборудования МФТС, установите для этого атрибута значение **true** при создании подсистемы захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты подсистемы захвата](capture-engine-attributes.md)
</dt> <dt>

[**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




