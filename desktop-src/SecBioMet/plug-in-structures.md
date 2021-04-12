---
title: Структуры подключаемых модулей
description: Структуры для разработки клиентских приложений с помощью API биометрическая платформа Windows.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API биометрическая платформа Windows API биометрическая платформа Windows, структуры подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331672"
---
# <a name="plug-in-structures"></a>Структуры подключаемых модулей

Для разработки клиентских приложений с помощью биометрическая платформа Windows API поддерживаются следующие структуры.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Политика учетных записей винбио \_**](winbio-account-policy.md)<br/>                                  | Содержит политику антиподмены по умолчанию или учетную запись.<br/>                                                         |
| [**\_ \_ версия интерфейса адаптера \_ винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Содержит основной и дополнительный номер версии, используемые в таблицах интерфейса модуля, датчика и адаптера хранилища.<br/>                |
| [**\_интерфейс ядра \_ винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Содержит указатели на функции пользовательского адаптера подсистемы.<br/>                                                                 |
| [**ВИНБИО \_ Расширенные \_ Параметры регистрации \_**](winbio-extended-enrollment-parameters.md)<br/> | Содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации. <br/>                            |
| [**\_конвейер винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Содержит общие контекстные сведения, используемые компонентами датчика, подсистемы и адаптера хранилища в одном биометрической единице.<br/> |
| [**\_интерфейс датчика \_ винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Содержит указатели на функции пользовательского адаптера датчика.<br/>                                                                 |
| [**\_интерфейс хранилища \_ винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Содержит указатели на пользовательские функции адаптера хранилища.<br/>                                                                |
| [**\_запись хранилища \_ винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Содержит биометрическое шаблон и связанные данные в стандартном формате.<br/>                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по подключаемым модулям](plug-in-reference.md)
</dt> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> <dt>

[**вбиокуеренгинеинтерфаце**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**вбиокуерисенсоринтерфаце**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**вбиокуеристоражеинтерфаце**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





