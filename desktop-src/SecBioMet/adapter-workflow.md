---
title: Рабочий процесс адаптера
description: В этом разделе описывается рабочий процесс регистрации с точки зрения подключаемых модулей адаптера.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79d018cfc853e8b92c1e9bd5400526fe0d425c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466021"
---
# <a name="adapter-workflow"></a>Рабочий процесс адаптера

В этом разделе описывается рабочий процесс регистрации с точки зрения подключаемых модулей адаптера.

в Windows 10 мы реализовали интерфейс механизма V4, который предоставляет 2 новые функции адаптера ядра, [**енгинеадаптеркреатекэй**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) и [**енгинеадаптеридентифифеатуресетсекуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn). Эти новые функции обеспечивают поддержку безопасных биометрических данных с помощью TPM 2,0. В следующей таблице показан рабочий процесс регистрации на стороне адаптера.




| | | API клиента | Методы адаптера | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Винбиожетпроперти (EXTENDED_ENGINE_INFO)</strong></a>  |  <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>Енгинеадаптеркуерекстендединфо</strong></a> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>Винбиоенроллбегин</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>сторажеадаптеркуерибисубжект</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>сенсорадаптерклеарконтекст</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>енгинеадаптеркреатинроллмент</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>енгинеадаптерсетенроллментпараметерс</strong></a></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"> <strong>Винбиоенроллкаптуре</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>сенсорадаптерстарткаптуре</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>сенсорадаптерфинишкаптуре</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>Сенсорадаптерпушдататоенгине</strong></a><strong>[- &gt; </strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>енгинеадаптеракцептсампледата</strong></a>]</li><li>Если S_OK или WINBIO_I_MORE_DATA<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>енгинеадаптерупдатинроллмент</strong></a></li><li>[Выполняется регистрация вызывающего объекта]</li></ol></li><li>Иначе, если WINBIO_E_BAD_CAPTURE [вызывающий объект отображает отзыв об отклонении, продолжение регистрации] <br /></li><li>Else, если другая ошибка<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></li><li>[Служба биографии прерывает регистрацию]</li></ol></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Винбиожетпроперти (EXTENDED_ENROLLMENT_STATUS)</strong></a>  |  <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>Енгинеадаптеркуерекстендеденроллментстатус</strong></a> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>Винбиоенроллкоммит</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>енгинеадаптерчеккфордупликате</strong></a></li><li>Если СЪЕМная база данных<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>енгинеадаптержетенроллменсаш</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>енгинеадаптеркоммитенроллмент</strong></a></li></ol></li><li>Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>енгинеадаптеркоммитенроллмент</strong></a><br /></li></ol> | | <a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"> <strong>Винбиоенроллдискард</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>енгинеадаптердискарденроллмент</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></li></ol> | 




 

 

 





