---
description: Пользовательские значения HRESULT для интерфейса записи диагностики графики.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537328"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Перечисление HRESULT

Пользовательские значения HRESULT для интерфейса записи диагностики графики.

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**  
Общее значение HRESULT, указывающее, что операция завершилась правильно.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**  
Общее значение HRESULT, указывающее, что операция выполнена успешно, но отличается от ожидаемой.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_файл ошибок \_ PIX \_ не \_ найден**  
Пользовательское значение HRESULT, которое отображает \_ файл ошибок, \_ не \_ найден.

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**Ошибка PIX "сбой \_ \_ \_ среды"**  
Пользовательское значение HRESULT, которое возвращает ошибку о \_ неправильной \_ среде.

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ неправильный формат ошибки \_ PIX**  
Пользовательское значение HRESULT, которое отображает ошибочный \_ \_ Формат ошибки.

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_ \_ нарушение общего доступа к ОШИБКАм PIX \_**  
Пользовательское значение HRESULT, которое выводит на экран \_ нарушение общего доступа к ошибкам \_ .

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_диск с ошибкой PIX \_ \_ полон**  
Пользовательское значение HRESULT, которое отображает \_ диск с ошибкой \_ Full.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**Ошибка PIX. \_ \_ Дополнительные \_ данные**  
Пользовательское значение HRESULT, которое отображает \_ Дополнительные данные об ошибке \_ .

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_Политика PIX E \_ Missing \_ \_ комплекты отладки \_**  
Пользовательское значение HRESULT, которое указывает на отсутствие политики комплектов отладки.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**\_ \_ Недопустимая версия PIX E \_**  
Пользовательское значение HRESULT, указывающее, что используется недопустимая версия.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ с использованием \_ дкомп**  
Пользовательское значение HRESULT, которое указывает, что DirectComposition используется (захват DirectComposition не поддерживается).

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ с использованием \_ DIRECTWRITE**  
Пользовательское значение HRESULT, которое указывает, что DirectWrite используется (захват DirectWrite не поддерживается).

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ с использованием \_ d3d9**  
Пользовательское значение HRESULT, которое указывает, что Direct3D9 используется (захват Direct3D9 не поддерживается в Windows 10).

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**не \_ \_ удается \_ создать \_ шейдер PIX E**  
Пользовательское значение HRESULT, указывающее, что невозможно создать заданный шейдер.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ использование \_ D2D**  
Пользовательское значение HRESULT, которое указывает, что Direct2D используется (захват Direct2D не поддерживается).

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ без \_ кадров**  
Пользовательское значение HRESULT, указывающее, что никакие кадры не были записаны.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ Отключить \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ в \_ win7**  
Пользовательское значение HRESULT, указывающее, что vsglog Windows 8 невозможно воспроизвести в Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_ \_ \_ Трассировка шейдера сборки PIX E \_**  
Пользовательское значение HRESULT, указывающее, что при построении трассировки шейдера произошла ошибка.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ без \_ \_ представления данных \_ CS**  
Пользовательское значение HRESULT, указывающее на отсутствие визуализации данных шейдера вычислений.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_ \_ пакет SDK для несоответствия PIX E \_**  
Пользовательское значение HRESULT, которое указывает на несоответствие текущего пакета SDK.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_ \_ возможный \_ пакет SDK для несоответствия PIX E \_**  
Пользовательское значение HRESULT, указывающее на возможное несоответствие текущего пакета SDK.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_ \_ необнаруживаемый пиксель PIX \_ E**  
Пользовательское значение HRESULT, указывающее на наличие необнаруживаемого пикселя.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**не \_ \_ удается выполнить \_ отладку \_ шейдера PIX E \_ с использованием \_ \_ \_ семантики системных значений**  
Пользовательское значение HRESULT, указывающее, что сахдер нельзя отлаживать с помощью семантики системных значений.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**\_УПДАТЕАВАИЛАБЛЕ PIX S \_**  
Пользовательское значение HRESULT, указывающее, что доступно обновление.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**состояние DXGI (PIX) \_ \_ \_ без \_ перенаправления**  
Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ без \_ перенаправления.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**\_ \_ состояние классической версии \_ PIX \_ без \_ доступа к рабочему столу**  
Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ без \_ доступа к рабочему столу \_ .

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ используемая Исходная графическая система \_ \_ PIX "состояние DXGI"**  
Пользовательское значение HRESULT, которое отображает \_ изображение состояния DXGI, \_ \_ \_ \_ \_ используемое источником VIDPN.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_ \_ \_ изменился режим состояния в режиме DXGI. \_**  
Пользовательское значение HRESULT, которое \_ \_ изменяет режим состояния DXGI \_ .

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ выполняется изменение режима состояния \_ \_ в режиме \_ DXGI.**  
Пользовательское значение HRESULT, которое отображает \_ \_ изменение режима состояния DXGI \_ \_ \_ .

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_состояние DXGI \_ в \_ унокклудед**  
Пользовательское значение HRESULT, которое отображает \_ состояние DXGI \_ унокклудед.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**\_ \_ \_ \_ \_ по-прежнему \_ рисуется состояние "PIX DXGI" ДДА**  
Пользовательское значение HRESULT, которое выводит на экран \_ состояние DXGI \_ ДДА \_ \_ \_ .

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ нотимпл**  
Пользовательское значение HRESULT, которое отображает E \_ нотимпл.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**неменяющий \_ интерфейс PIX E \_**  
Пользовательское значение HRESULT, которое отображает \_ интерфейс E.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_указатель электронной почты PIX \_**  
Пользовательское значение HRESULT, которое возвращает \_ указатель E.

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**\_прерывание от PIX E \_**  
Пользовательское значение HRESULT, которое выводит на экран электронное \_ прерывание.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**\_сбой PIX E \_**  
Пользовательское значение HRESULT, которое возвращает E \_ Failed.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**\_ \_ непредвиденная E PIX**  
Пользовательское значение HRESULT, которое отображает \_ непредвиденные результаты в E.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**  
Пользовательское значение HRESULT, которое отображает E \_ ACCESSDENIED.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_описатель E \_ PIX**  
Пользовательское значение HRESULT, которое отображает E- \_ маркер.

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**  
Пользовательское значение HRESULT, которое отображает E \_ OUTOFMEMORY.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
Пользовательское значение HRESULT, которое отображает E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**диск "PIX", \_ \_ Ошибка Xbox \_ \_ полон**  
Пользовательское значение HRESULT, указывающее на то, что диск заполнен.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ \_ используемый адрес PIX WS \_ E \_**  
Пользовательское значение HRESULT, указывающее, что адрес уже используется.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_ \_ \_ Политика отсутствующих \_ наборов \_ пакетов PIX WS E**  
Пользовательское значение HRESULT, указывающее, что адрес недоступен.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ TE \_ фаиледтолоадсофтваремодуле**  
Пользовательское значение HRESULT, указывающее, что не удалось загрузить необходимый программный модуль.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ TE \_ уседсофтваремодулесатваснтварпорреф**  
Пользовательское значение HRESULT, указывающее, что используемый программный модуль не является драйвером деформации или ссылки.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ TE \_ корруптедфиле**  
Пользовательское значение HRESULT, указывающее, что файл поврежден.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ TE \_ фаиледтупенфиле**  
Пользовательское значение HRESULT, указывающее, что не удалось открыть файл.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ TE \_ каллфаиледонплайбакк**  
Пользовательское значение HRESULT, указывающее на сбой вызова во время воспроизведения.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ TE \_ ункновнууид**  
Пользовательское значение HRESULT, указывающее, что обнаружен неизвестный идентификатор UUID; Это не должно происходить.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ TE \_ ноткаптурефилеоркорруптед**  
Пользовательское значение HRESULT, указывающее, что файл не является файлом записи или поврежден.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ TE \_ неверфиле**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ TE \_ олдерфиле**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ TE \_ инвалидмомент**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_ \_ неверный драйвер PIX TE \_**  
Пользовательское значение HRESULT, указывающее, что драйвер является недопустимым.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**Ошибка PIX не \_ \_ удается \_ получить доступ к \_ депсстенЦил \_ в \_ ЦП**  
Пользовательское значение HRESULT, указывающее, что ЦП попытался получить доступ к буферу шаблона глубины, что привело к ошибке.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**Ошибка PIX не \_ \_ удается \_ Разрешить \_ многовыборочную \_ текстуру**  
Пользовательское значение HRESULT, указывающее, что была предпринята попытка разрешить многовыборочную текстуру, что привело к ошибке.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_ \_ Ошибка \_ неправильного \_ вызова PIX DXGI**  
Пользовательское значение HRESULT, которое отображает \_ \_ недопустимый вызов ошибки DXGI \_ .

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_ \_ \_ не \_ удалось найти ошибку DXGI PIX**  
Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI, \_ не \_ найдено.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ Дополнительные данные об ошибке PIX DXGI \_**  
Пользовательское значение HRESULT, которое отображает \_ Дополнительные данные об ошибке DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**Ошибка "PIX \_ DXGI" \_ \_ не поддерживается**  
Пользовательское значение HRESULT, которое \_ не поддерживает вывод ошибок DXGI \_ .

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_устройство с ошибкой PIX DXGI \_ \_ \_ удалено**  
Пользовательское значение HRESULT, которое отображает \_ устройство с ошибкой DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_Ошибка в \_ устройстве DXGI для устройства с \_ \_ зависанием**  
Пользовательское значение HRESULT, которое отображает \_ \_ \_ зависание устройства DXGI.

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_ \_ Восстановление устройства с ошибками PIX DXGI \_ \_**  
Пользовательское значение HRESULT, которое отображает \_ Сброс устройства с ошибкой DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**Ошибка в PIX \_ DXGI \_ \_ \_ \_**  
Пользовательское значение HRESULT, которое \_ \_ \_ по-прежнему отображает ошибку DXGI \_ .

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**несвязанная \_ \_ \_ Статистика кадра ошибок \_ \_ DXGI PIX**  
Пользовательское значение HRESULT, которое отображает несвязанную \_ \_ статистику кадра ошибок DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ используемый источник VIDPN \_ для \_ графики ошибок DXGI PIX**  
Пользовательское значение HRESULT, которое отображает \_ \_ \_ используемый источник VIDPN для графики ошибок DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ \_ Внутренняя ошибка в драйвере системы PIX DXGI \_**  
Пользовательское значение HRESULT, которое отображает \_ \_ внутреннюю ошибку драйвера DXGI Error \_ \_ .

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**\_Ошибка PIX DXGI — \_ \_ Немонопольная**  
Пользовательское значение HRESULT, которое отображает ошибку DXGI, не \_ \_ исключающее.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_ \_ Ошибка \_ \_ в недоступном в настоящий момент в \_ PIX DXGI**  
Пользовательское значение HRESULT, которое отображает \_ ошибку \_ DXGI \_ в данный момент \_ недоступно.

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**Ошибка в PIX \_ DXGI " \_ \_ Удаленный \_ клиент \_ отключен"**  
Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI \_ Remote \_ Client \_ disconnected.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_Ошибка PIX \_ DXGI \_ Remote \_ OUTOFMEMORY**  
Пользовательское значение HRESULT, которое отображает \_ ошибку DXGI \_ Remote \_ OUTOFMEMORY.

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ выполняется изменение режима ошибок \_ DXGI \_ в режиме ошибки \_**  
Пользовательское значение HRESULT, которое отображает \_ \_ изменение режима ошибок DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ \_ потеряна доступ к ошибке PIX DXGI \_**  
Пользовательское значение HRESULT, которое выводит на экран \_ доступ к ошибке DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ время ожидания при ошибке PIX DXGI \_**  
Пользовательское значение HRESULT, которое отображает \_ \_ \_ время ожидания ошибки DXGI.

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_ \_ сеанс ошибки DXGI \_ PIX \_ отключен**  
Пользовательское значение HRESULT, которое отображает \_ сеанс с ошибкой DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**Ошибка "PIX \_ DXGI" \_ \_ \_ , ограничение на \_ вывод \_ устаревшей**  
Пользовательское значение HRESULT, которое отображает \_ ошибку \_ DXGI \_ с ограничением в \_ OUTPUT \_ .

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**Ошибка в PIX \_ DXGI \_ \_ не может \_ защитить \_ содержимое**  
Пользовательское значение HRESULT, которое возвращает \_ ошибку DXGI, \_ не может \_ защитить \_ содержимое.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ отказано в доступе к ошибке PIX DXGI \_**  
Пользовательское значение HRESULT, которое отображает \_ ошибку в \_ доступе к DXGI \_ .

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**\_ \_ имя ошибки PIX \_ DXGI \_ уже \_ существует**  
Пользовательское значение HRESULT, которое отображает \_ имя ошибки DXGI, \_ \_ уже \_ существует.

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_ \_ \_ отсутствует компонент пакета SDK для ошибки \_ DXGI PIX \_**  
Пользовательское значение HRESULT, которое выводит на экран \_ \_ компонент пакета SDK ошибок DXGI \_ \_ .

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_ \_ васстиллдравинг Err для DDI DXGI \_ \_**  
Пользовательское значение HRESULT, которое выводит на экран DXGI \_ \_ \_ васстиллдравинг Err.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_ \_ \_ неподдерживаемая ошибка в DDI DXGI PIX \_**  
Пользовательское значение HRESULT, которое выводит на экран \_ ошибку DDI DXGI \_ \_ не поддерживается.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_ \_ \_ неисключительная ошибка в DDI DXGI PIX \_**  
Пользовательское значение HRESULT, которое выводит на экран \_ ошибку DDI DXGI \_ \_ .

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**\_Ошибка PIX D3D10. \_ \_ слишком \_ много \_ уникальных \_ \_ объектов состояния**  
Пользовательское значение HRESULT, которое выводит на экран D3D10 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов состояния.

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ Файл ошибки PIX \_ D3D10 \_ не \_ найден**  
Пользовательское значение HRESULT, которое \_ \_ \_ не удалось найти, D3D10 файл ошибок \_ .

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**\_Ошибка PIX D3D11. \_ \_ слишком \_ много \_ уникальных \_ \_ объектов состояния**  
Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов состояния.

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ Файл ошибки PIX \_ D3D11 \_ не \_ найден**  
Пользовательское значение HRESULT, которое \_ \_ \_ не удалось найти, D3D11 файл ошибок \_ .

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Ошибка PIX D3D11 \_ при \_ слишком \_ большом количестве \_ уникальных \_ \_ объектов представления**  
Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ ошибку \_ слишком \_ много \_ уникальных \_ \_ объектов представления.

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX \_ D3D11 \_ Error \_ Отложенная \_ \_ схема контекста \_ без \_ начального \_ удаления**  
Пользовательское значение HRESULT, которое выводит на экран D3D11 \_ \_ отложенную \_ \_ карту контекста \_ без \_ начального \_ удаления.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**\_Ошибка PIX \_ перекрыто \_ \_ вызов Draw**  
Пользовательское значение HRESULT, указывающее, что вызов Draw был полностью перекрыто, что привело к ошибке.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



