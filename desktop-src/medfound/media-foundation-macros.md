---
description: Media Foundation макросов
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: Media Foundation макросов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bed83710f41957edc1b945fecd5d68b5550b4ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999868"
---
# <a name="media-foundation-macros"></a>Media Foundation макросов

## <a name="in-this-section"></a>Содержание раздела



| attribute                                                                                              | Описание                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ОПРЕДЕЛЕНИЕ \_ \_ GUID MEDIATYPE**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | Определяет GUID подтипа носителя из кода FOURCC, значения **D3DFORMAT** или типа звукового формата.<br/>                                                                       |
| [**\_событие получения \_ \_ \_ учетных данных \_ МФП Get**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ \_ события получения учетных данных пользователя МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event) .<br/> |
| [**\_ \_ событие ошибки получения \_ МФП**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ события ошибки МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event) .<br/>                                       |
| [**\_ \_ \_ событие шага получения кадра \_ МФП**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ события шага МФП Frame**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event) .<br/>                            |
| [**\_ \_ \_ событие очистки МФП Get \_ MEDIAITEM**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к пустому указателю [**\_ \_ события MEDIAITEM**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event) .<br/>                   |
| [**\_событие МФП Get \_ MEDIAITEM \_ Created \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**события МФП \_ MEDIAITEM \_ Created \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event) .<br/>              |
| [**МФП \_ Get \_ MEDIAITEM \_ Set, \_ событие**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ события MEDIAITEM Set МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) .<br/>                      |
| [**МФП \_ Получение \_ \_ события MF**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**событий МФП \_ MF \_**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) .<br/>                                              |
| [**МФП \_ получить \_ событие приостановки \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ события приостановки МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) .<br/>                                       |
| [**МФП \_ получить \_ \_ событие воспроизведения**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ события воспроизведения МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .<br/>                                         |
| [**\_ \_ \_ событие завершения воспроизведения \_ МФП**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ события завершения воспроизведения МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event) .<br/>                    |
| [**МФП \_ получить \_ \_ событие установки \_ должности**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ события установки позиции МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event) .<br/>                        |
| [**\_ \_ \_ событие установки скорости получения \_ МФП**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ \_ события установки скорости МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) .<br/>                                |
| [**МФП \_ получить \_ \_ событие завершения**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | Приводит указатель [**\_ \_ заголовка события МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) к указателю [**\_ \_ события завершения МФП**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) .<br/>                                         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по программированию в Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
