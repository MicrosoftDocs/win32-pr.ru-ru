---
description: Указывает, что кодировщик MFT поддерживает получение событий Минкодингпараметер во время потоковой передачи.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Атрибут MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a528da44d59077c8445616f8fe344cba5497ced8b33be75e33be71bf9b5d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113044"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>\_КОДИРОВЩИК MFT \_ поддерживает \_ \_ атрибут события конфигурации

Указывает, что кодировщик MFT поддерживает получение событий [минкодингпараметер](meencodingparameters.md) во время потоковой передачи.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Отправляется кодировщиком MFT через [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мфтрансформ. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфтрансформ::P Роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




