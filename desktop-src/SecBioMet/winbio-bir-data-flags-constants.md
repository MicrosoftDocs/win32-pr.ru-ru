---
title: Константы WINBIO_BIR_DATA_FLAGS (Винбио \_ types. h)
description: Укажите условие для данных.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622634"
---
# <a name="winbio_bir_data_flags-constants"></a>\_ \_ \_ Константы флагов данных винбио Бир

Следующие константы используются элементом " **Флаги** данных" в структуре [**заголовка винбио \_ Бир \_**](winbio-bir-header.md) .



| Константа/значение                                                                                                                                                                                                                                                                                   | Описание                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**Винбио \_ \_ \_ Конфиденциальность флагов данных**</dt> <dt>0x02</dt> </dl>                                       | Данные зашифрованы.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**Винбио \_ \_ \_ Целостность ФЛАГов данных**</dt> — <dt>0x01</dt> </dl>                                 | Данные имеют цифровую подпись или защищаются с помощью кода проверки подлинности сообщений (MAC).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**Винбио \_ Флаг данных, \_ \_ подписанный**</dt> <dt>0x04</dt> </dl>                                          | Если установлен этот флаг и **флаг \_ \_ \_ целостности флага данных винбио** , данные подписываются. Если этот флаг не установлен, но установлен **флаг \_ \_ \_ целостности флага данных винбио** , то для данных будет рассчитан Mac.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**Винбио \_ \_ \_ Необработанный флаг данных**</dt> <dt>0x20</dt> </dl>                                                   | Данные имеют формат, с которым они были захвачены.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**Винбио \_ \_Флаг данных \_ промежуточный**</dt> <dt>0x40</dt> </dl>                        | Данные не являются необработанными, но обработаны не полностью.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**Винбио \_ \_ \_ Обработанный флаг данных**</dt> <dt>0x80</dt> </dl>                                 | Данные обработаны.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**Винбио \_ \_Маска параметра флага данных \_ \_ \_ представляет**</dt> собой <dt>0x08</dt> </dl> | Маска флага. Это значение всегда равно единице (1).<br/>                                                                                                                                                           |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





