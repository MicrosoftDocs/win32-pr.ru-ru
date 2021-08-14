---
description: В выходных данных диспетчера защиты (ОПМ) используются следующие структуры.
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Структуры ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737651"
---
# <a name="opm-structures"></a>Структуры ОПМ

В [выходных данных диспетчера защиты](output-protection-manager.md) (ОПМ) используются следующие структуры.



| Структура                                                                                              | Описание                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_заголовок GRL**](grl-header.md)                                                                      | Содержит заголовок глобального списка отзыва (GRL).                                                                                                          |
| [**\_подпись MF**](mf-signature.md)                                                                  | Содержит сигнатуру глобального списка отзыва (GRL).                                                                                                         |
| [**ОПМ \_ ACP \_ и \_ кгмса \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Содержит результаты запроса на [**\_ получение сигнала ОПМ \_ для \_ ACP \_ и \_ кгмса**](opm-get-acp-and-cgmsa-signaling.md) .                                         |
| [**ОПМ \_ фактический \_ выходной \_ Формат**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Содержит результат запроса [**ОПМ \_ получения \_ фактического \_ \_ формата выходных данных**](opm-get-actual-output-format.md) в выходных данных диспетчера защиты (ОПМ).               |
| [**ОПМ \_ Настройка \_ параметров**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Содержит команду ОПМ или сертифицированный выходной Protection Manager (Копп).                                                                                     |
| [**\_ \_ \_ сведения о подключенном устройстве HDCP \_ ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Содержит результат из [**\_ информационного запроса ОПМ Get \_ Connected \_ HDCP \_ Device \_**](opm-get-connected-hdcp-device-information.md) .                     |
| [**\_ \_ \_ \_ Параметры получения сведений о совместимости ОПМ Копп \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Содержит параметры для метода [**иопмвидеуутпут:: коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) . |
| [**ОПМ \_ \_ параметры инициализации \_ шифрования**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Содержит параметры инициализации для сеанса ОПМ.                                                                                                     |
| [**ОПМ \_ получить \_ сведения о кодека \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Содержит результат из запроса на [**\_ Получение \_ \_ сведений о коде ОПМ**](opm-get-codec-info.md) .                                                                     |
| [**ОПМ \_ получить \_ \_ Параметры сведений о кодека \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Содержит сведения о команде [**ОПМ \_ Get \_ кодека \_**](opm-get-codec-info.md) .                                                                  |
| [**\_Параметры получения \_ сведений о \_ ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Содержит параметры для метода [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) out.                             |
| [**\_ \_ \_ вектор выбора ключа HDCP \_ ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Содержит вектор выбора ключа (КСВ) для приемника High-Bandwidth цифрового Защита содержимого (HDCP).                                                   |
| [**ОПМ \_ ОМАК**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Содержит код проверки подлинности сообщения (MAC) для сообщения ОПМ.                                                                                           |
| [**\_ \_ данные идентификатора выхода \_ ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Содержит результат запроса на [**Получение состояния \_ \_ \_ идентификатора выхода ОПМ**](opm-get-output-id.md) .                                                              |
| [**\_случайное \_ число ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Содержит 128-разрядное случайное число для использования с ОПМ.                                                                                                         |
| [**ОПМ \_ запрошенные \_ сведения**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Содержит результат запроса состояния ОПМ.                                                                                                              |
| [**\_ \_ \_ \_ \_ Параметры сигнализации ОПМ Set ACP и \_ кгмса**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Содержит сведения о команде [**ОПМ \_ Set \_ ACP \_ и \_ кгмса \_**](opm-set-acp-and-cgmsa-signaling.md) в ОПМ.                               |
| [**ОПМ \_ Установка \_ \_ параметров СРМ \_ HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Содержит параметры для команды [**ОПМ \_ Set \_ HDCP \_ СРМ**](opm-set-hdcp-srm.md) .                                                                       |
| [**ОПМ \_ задать \_ \_ Параметры уровня \_ защиты**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Содержит данные для команды [ОПМ \_ Set \_ Protection \_ Level](opm-set-protection-level.md) в ОПМ.                                                          |
| [**\_стандартные \_ сведения ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Содержит результат запроса состояния ОПМ.                                                                                                            |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по программированию ОПМ](opm-programming-reference.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 



