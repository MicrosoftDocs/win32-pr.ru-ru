---
description: Определяет идентификаторы ресурсов для общих строковых ресурсов.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5012a6dc40f47a396139eb29f2f88151b4a10ffb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623160"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>\_Перечисление идентификаторов ресурсов

Определяет идентификаторы ресурсов для общих строковых ресурсов. Они передаются подсистеме захвата из узла. они используются для вывода строк в наложение HUD передаваемого приложения или для передачи значений реестра из параметров Visual Studio в запись енги

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ИДЕНТИФИКАТОРы \_ енгинедисконнектед**  
Не используется. Идентификатор ресурса для строки ранее использовался, чтобы указать, что принтскрин был достигнут после завершения сеанса записи.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**  
Не используется.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**ИДЕНТИФИКАТОРы \_ дефаултекспфиле \_ содержимого**  
Не используется. Идентификатор ресурса для строки ранее использовался для XML-данных в сценариях записи прежних версий.

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_сообщение захвата идентификаторов \_**  
Идентификатор ресурса для строки "захваченный кадр".

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**запись ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается**  
Идентификатор ресурса для строки "Эта программа сообщила, что ее нельзя использовать с диагностика графики инструментами".

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**Заголовок "запись ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается \_ "**  
Идентификатор ресурса для строки "неподдерживаемые функции"

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**Функция ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается**  
Идентификатор ресурса для строки "уровень компонентов устройства не поддерживается"

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дксверсион \_ не \_ поддерживаются**  
Идентификатор ресурса для строки "версия DirectX не подписывается"

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дкомп \_ не \_ поддерживаются**  
Идентификатор ресурса для строки "ДКОМП используется приложением, но не поддерживается в этой ОС"

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дврите \_ не \_ поддерживаются**  
Идентификатор ресурса для строки "ДВРИТЕ используется приложением, но не поддерживается в этой ОС"

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**ИДЕНТИФИКАТОРы \_ ожидаемого \_ \_ формата сбоя**  
Идентификатор ресурса для строки "% s" вернул ошибку во время воспроизведения. (HRESULT =% s) \\ r \\ n ".

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**Идентификатор \_ \_ сообщения каптуретултип**  
Идентификатор ресурса для строки "используйте параметр" Печать экрана "для записи кадра."

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**ИДЕНТИФИКАТОРы \_ D2D \_ и \_ D10 \_ не \_ поддерживаются**  
Идентификатор ресурса для строки "D2D и D10 не поддерживаются вместе в этой ОС"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**\_Статистика HUDности идентификаторов \_**  
Идентификатор ресурса для строки "кадров перехвачено% d". Время кадра (МС)% 0.00 f "

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**\_внутренний \_ метод ID**  
Идентификатор ресурса для строки "внутренний метод DirectX"

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_ \_ метки кадра захвата идентификаторов \_**  
Идентификатор ресурса для строки "захваченный кадр% ld"

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**ПИПЕЛИНЕСТАЖЕ \_ инпутассемблер**  
Не используется.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ вертексшадер**  
Не используется.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ хуллшадер**  
Не используется.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**ПИПЕЛИНЕСТАЖЕ \_ тесселатор**  
Не используется.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ домаиншадер**  
Не используется.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ жеометришадер**  
Не используется.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**ПИПЕЛИНЕСТАЖЕ \_ стреамаутпут**  
Не используется.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**средство программной \_ прорисовки пипелинестаже**  
Не используется.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ PIXELSHADER**  
Не используется.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**ПИПЕЛИНЕСТАЖЕ \_ аутпутмержер**  
Не используется.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ компутешадер**  
Не используется.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**БУФФЕРОБЖЕКТ \_ суппортедформат**  
Не используется.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**БУФФЕРОБЖЕКТ \_ куррентформат**  
Не используется.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_заголовок буфферобжект**  
Не используется.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**БУФФЕРОБЖЕКТ \_ строка**  
Не используется.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**БУФФЕРОБЖЕКТ \_ инвалидформат**  
Не используется.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**БУФФЕРОБЖЕКТ \_ инвалидемптиформат**  
Не используется.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**БУФФЕРОБЖЕКТ \_ инвалидформатсизе**  
Не используется.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**СУММАРИНФО \_ таржетаппликатион**  
Текст, отображаемый в окне "свойства vsglog" — целевое приложение

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**\_путь суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Path

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**СУММАРИНФО \_ TARGETVERSION**  
Текст, отображаемый в vsglog окно свойств — Целевая версия

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**СУММАРИНФО \_ LASTMODIFIEDDATE**  
Текст, отображаемый в vsglog окно свойств — Дата последнего изменения

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**Идентификатор \_ процесса суммаринфо**  
Текст, отображаемый в vsglog окно свойств — идентификатор процесса

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**СУММАРИНФО \_ експериментфиле**  
Текст, отображаемый в файле vsglog окно свойств-эксперименте

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**СУММАРИНФО \_ рунфиле**  
Текст, отображаемый в файле vsglog окно свойств-Run

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**\_Размер суммаринфо**  
Текст, отображаемый в vsglog окно свойств-size

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**СУММАРИНФО \_ креатедбипиксверсион**  
Текст, отображаемый в vsglog окно свойств, созданная по версии

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**СУММАРИНФО \_ сессионстарттиме**  
Текст, отображаемый в vsglog окно свойств — время начала сеанса

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**СУММАРИНФО \_ SYSTEMINFORMATION**  
текст, отображаемый в окно свойств vsglog — Сведения о системе

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_процессор суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Processor

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_память суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Memory

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**СУММАРИНФО \_ OSVersion**  
Текст, отображаемый в vsglog окно свойств — версия ОС

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**СУММАРИНФО \_ осарчитектуре**  
Текст, отображаемый в архитектуре окно свойств vsglog-OS

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**СУММАРИНФО \_ таржетаппарчитектуре**  
Текст, отображаемый в архитектуре vsglog окно свойств-Target App

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**СУММАРИНФО \_ максхвфеатурелевел**  
Текст, отображаемый в vsglog окно свойств — максимальный уровень компонентов оборудования

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**СУММАРИНФО \_ дриверконкурренткреатес**  
Текст, отображаемый в параллельном создании драйвера vsglog окно свойств-Driver

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**СУММАРИНФО \_ дриверкоммандлистс**  
Текст, отображаемый в списках команд vsglog окно свойств-Driver

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**СУММАРИНФО \_ даублепреЦисионшадерс**  
Текст, отображаемый в vsglog окно свойств-шейдеры двойной точности

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**СУММАРИНФО \_ DIRECTCOMPUTECS4X**  
Текст, отображаемый в vsglog окно свойств-Direct COMPUTE CS 4. x

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**СУММАРИНФО \_ 10BITXRHIGHCOLORFORMAT**  
Текст, отображаемый в vsglog окно свойств-10BITXRHIGHCOLORFORMAT

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**СУММАРИНФО \_ екстендедколорформатсуппорт**  
Текст, отображаемый в окно свойств vsglog. Поддержка расширенного формата цвета

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**СУММАРИНФО \_ DISPLAYINFORMATION**  
Текст, отображаемый в vsglog окно свойств-Отображение информации

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**СУММАРИНФО \_ дисплайнинформатион**  
Текст, отображаемый в vsglog окно свойств-дисплей N, сведения

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**\_имя суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Name

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**\_Описание суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Description

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**СУММАРИНФО \_ дисплаймемори**  
Текст, отображаемый в vsglog окно свойств-отображать память

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**СУММАРИНФО \_ имя_драйвера**  
Текст, отображаемый в vsglog окно свойств-Driver Name

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**СУММАРИНФО \_ дриверверсион**  
Текст, отображаемый в версии драйвера окно свойств vsglog

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**СУММАРИНФО \_ модулеинформатион**  
Текст, отображаемый в сведениях о модуле окно свойств vsglog-Module

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**СУММАРИНФО \_ DIRECT3DINFORMATION**  
Текст, отображаемый в vsglog окно свойств — сведения о Direct3D

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**СУММАРИНФО \_ всгверсион**  
Текст, отображаемый в vsglog окно свойств — версия VSG

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**СУММАРИНФО \_ каптуремачине**  
Текст, отображаемый на компьютере vsglog окно свойств-Capture

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**СУММАРИНФО \_ плайбаккмачине**  
Текст, отображаемый на компьютере vsglog окно свойств-воспроизведения

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**СУММАРИНФО \_ REMOTEDATA**  
Текст, отображаемый в vsglog окно свойств — удаленные данные

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**СУММАРИНФО \_ OtherDirect3DInformation**  
Текст, отображаемый в vsglog окно свойств — другие сведения о Direct3D

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**СУММАРИНФО \_ сизегб**  
Текст, отображаемый в vsglog окно свойств-size ГБ

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**СУММАРИНФО \_ сиземб**  
Текст, отображаемый в vsglog окно свойств — размер Мб

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**СУММАРИНФО \_ сизебитес**  
Текст, отображаемый в vsglog окно свойств размером байт

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**СУММАРИНФО \_ MEMORYMB**  
Текст, отображаемый в vsglog окно свойств памяти, МБ

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**СУММАРИНФО \_ x86**  
Текст, отображаемый в vsglog окно свойств — x86

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**СУММАРИНФО \_ x64**  
Текст, отображаемый в vsglog окно свойств x64

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**СУММАРИНФО \_ true**  
Текст, отображаемый в vsglog окно свойств — true

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**СУММАРИНФО \_ false**  
Текст, отображаемый в vsglog окно свойств-false

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**СУММАРИНФО \_ ARM32**  
Текст, отображаемый в vsglog окно свойств-ARM 32

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**СУММАРИНФО \_ ункновнкпуарчитектуре**  
Текст, отображаемый в vsglog окно свойств — Неизвестная архитектура ЦП

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**СУММАРИНФО \_ аллдксгиформатвалуес**  
Текст, отображаемый в vsglog окно свойств — все значения формата DXGI

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**СУММАРИНФО \_ AllD3D11FormatSupportValues**  
Текст, отображаемый в vsglog окно свойств — все значения поддержки формата D3D11

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**\_ \_ Потоки функций суммаринфо \_ D3D11**  
Текст, отображаемый в \_ многопоточной функции vsglog окно свойств-D3D11 \_

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**СУММАРИНФО \_ DriverConcurrentCreates1**  
Текст, отображаемый в параллельном vsglog окно свойств-драйвере, создает 1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**СУММАРИНФО \_ DriverCommandLists1**  
Текст, отображаемый в команде vsglog окно свойств-Driver, содержит список 1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**СУММАРИНФО \_ D3D11 \_ функция \_ Double**  
Текст, отображаемый в функции vsglog окно свойств-D3D11, \_ \_ удваивается

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**СУММАРИНФО \_ даублепреЦисионфлоатшадеропс**  
Текст, отображаемый в операциях шейдера vsglog окно свойств с двойной точностью с плавающей запятой

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ D3D10 \_ X \_ \_ Параметры оборудования**  
Текст, отображаемый в vsglog окно свойств- \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Параметры оборудования

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**СУММАРИНФО \_ компутешадерс \_ Plus \_ равандструктуредбуфферс \_ через \_ шейдер \_ 4 \_ x**  
Текст, отображаемый в vsglog окно свойств-Компутешадерс + RAW и Structure Дбуфферс через шейдер 4. x

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**\_ \_ Параметры D3D11 для функции суммаринфо D3D11 \_ \_**  
Текст, отображаемый в \_ \_ параметрах D3D11 vsglog окно свойств-D3D11 Feature \_

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**СУММАРИНФО \_ аутпутмержерлогикоп**  
Текст, отображаемый в операции логики слияния vsglog окно свойств-Output

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**СУММАРИНФО \_ уавонлирендерингфорцедсамплекаунт**  
Текст, отображаемый в vsglog окно свойств-UAV, выводит число принудительных выборок.

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**СУММАРИНФО \_ дискардаписсинбидривер**  
Текст, отображаемый в API vsglog окно свойств-Discard, показанный драйвером

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**СУММАРИНФО \_ флагсфорупдатеандкописинбидривер**  
Текст, отображаемый в vsglog окно свойств-флаги для обновления и копирования, отображаемый драйвером

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**СУММАРИНФО \_ клеарвиев**  
Текст, отображаемый в vsglog окно свойств — очистить представление

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**СУММАРИНФО \_ копивисоверлап**  
Текст, отображаемый в vsglog окно свойств-Copy с перекрытием

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**СУММАРИНФО \_ константбуфферпартиалупдате**  
Текст, отображаемый в частичном обновлении буфера vsglog окно свойств-Constant

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**СУММАРИНФО \_ константбуффероффсеттинг**  
Текст, отображаемый в vsglog окно свойств-константном буфере смещения

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**СУММАРИНФО \_ мапнувервритеондинамикконстантбуффер**  
Текст, отображаемый в vsglog окно свойств-Map без перезаписи в динамическом буфере константы

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**СУММАРИНФО \_ мапнувервритеондинамикбуфферсрв**  
Текст, отображаемый в vsglog окно свойств-Map без перезаписи в динамическом буфере SRV

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**СУММАРИНФО \_ мултисамплертввисфорцедсамплекаунтоне**  
Текст, отображаемый в vsglog окно свойств — многопримерный РТВ с принудительным числом выборок, один

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**СУММАРИНФО \_ SAD4ShaderInstructions**  
Текст, отображаемый в инструкциях шейдера vsglog окно свойств-SAD4

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**СУММАРИНФО \_ екстендеддаублесшадеринструктионс**  
Текст, отображаемый в инструкциях vsglog окно свойств — расширенные двойные шейдеры

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**СУММАРИНФО \_ екстендедресаурцешаринг**  
Текст, отображаемый в vsglog окно свойств — расширенный общий доступ к ресурсам

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_ \_ \_ Сведения об архитектуре функций суммаринфо D3D11 \_**  
Текст, отображаемый в \_ \_ сведениях об архитектуре функций vsglog окно свойств-D3D11 \_

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**СУММАРИНФО \_ тилебаседдеферредрендерер**  
Текст, отображаемый в окно свойств vsglog отложенного модуля подготовки отчетов на основе плиток

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**\_ \_ Параметры d3d9 для функции суммаринфо D3D11 \_ \_**  
Текст, отображаемый в \_ \_ параметрах D3D9 vsglog окно свойств-D3D11 Feature \_

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**СУММАРИНФО \_ FullNonPow2TextureSupport**  
Текст, отображаемый в vsglog окно свойств — полная поддержка текстур без Pow2

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**\_ \_ \_ \_ Поддержка min суммаринфо для шейдера функций D3D11 \_ \_**  
Текст, отображаемый в vsglog окно свойств-D3D11, \_ Поддержка функции \_ \_ min Shader \_ \_

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**СУММАРИНФО \_ пикселшадерминпреЦисион**  
Текст, отображаемый в окно свойств vsglog, минимальная точность шейдера пикселей

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**СУММАРИНФО \_ аллосершадерстажесминпреЦисион**  
Текст, отображаемый на vsglog окно свойств-все остальные этапы минимальной точности шейдеров

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**\_ \_ \_ \_ Поддержка теневого копирования d3d9 компонентов суммаринфо D3D11 \_**  
Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ d3d9, \_ Поддержка теневого копирования \_

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**СУММАРИНФО \_ суппортсдепсастекстуревислессекуалкомпарисонфилтер**  
Текст, отображаемый в vsglog окно свойств, поддерживает глубину в виде текстуры с фильтром сравнения "меньше чем равно"

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**  
Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ D3D11 \_ OPTIONS1

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**СУММАРИНФО \_ тиледресаурцестиер**  
Текст, отображаемый на уровне vsglog окно свойств-мозаичных ресурсов

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**СУММАРИНФО \_ минмаксфилтеринг**  
Текст, отображаемый в vsglog окно свойств-min max Filter

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**СУММАРИНФО \_ клеарвиевалсосуппортсдепсонлиформатс**  
Текст, отображаемый в vsglog окно свойств-Clear представление, также поддерживает форматы только глубины

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**СУММАРИНФО \_ мапондефаултбуфферс**  
Текст, отображаемый в vsglog окно свойств-Map в буферах по умолчанию

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**\_ \_ \_ \_ Поддержка простого создания \_ экземпляров \_ в суммаринфо D3D11 Feature d3d9**  
Текст, отображаемый в функции vsglog окно свойств-D3D11 \_ \_ d3d9 Simple для создания \_ \_ экземпляров \_

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**СУММАРИНФО \_ SimpleInstancingSupported0**  
Текст, отображаемый в vsglog окно свойств — простой создание экземпляров, поддерживается 0

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_ \_ \_ Поддержка маркеров компонентов D3D11 \_ суммаринфо**  
Текст, отображаемый в окно свойств vsglog-D3D11, \_ \_ поддерживает маркеры компонентов. \_

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Профиль суммаринфо**  
Текст, отображаемый в vsglog окно свойств-Profile

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ d3d9 \_ OPTIONS1**  
Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ d3d9 \_ OPTIONS1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**СУММАРИНФО \_ FullNonPow2TextureSupported**  
Текст, отображаемый в vsglog окно свойств-Full (неPow2ная текстура)

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**СУММАРИНФО \_ депсастекстуревислессекуалкомпарисонфилтерсуппортед**  
Текст, отображаемый в vsglog окно свойств-Depth как текстура с поддержкой фильтра менее одинаковых сравнений

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**СУММАРИНФО \_ SimpleInstancingSupported1**  
Текст, отображаемый в vsglog окно свойств — поддержка простого создания экземпляров 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**СУММАРИНФО \_ текстурекубефацерендертаржетвиснонкубедепсстенЦилсуппортед**  
Текст, отображаемый на поверхности vsglog окно свойств-текстурный куб, не поддерживает набор элементов глубины Куба

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**СУММАРИНФО \_ дксгиформат**  
Текст, отображаемый в vsglog окно свойств-Дксгиформат

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**СУММАРИНФО \_ DXGIFormat1**  
Текст, отображаемый в vsglog окно свойств-DXGIFormat1

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**СУММАРИНФО \_ ModuleName**  
Текст, отображаемый в vsglog окно свойств-MODULENAME

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**\_Конфигурация Идд**  
Текст, отображаемый в диалоговом окне настройки брандмауэра в Всграфиксремотингине

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_значок статического \_ заголовка \_ IDC**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра-статический заголовок"

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_статический \_ заголовок IDC**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — статический заголовок

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_Конфигурация статического \_ встроенного по IDC \_**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Конфигурация статического брандмауэра

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_значок статического \_ встроенного по IDC \_**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — значок "статический брандмауэр"

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_заголовок статического \_ встроенного по IDC \_**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — статический заголовок брандмауэра

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_встроенное по "static GROUPBOX" IDC \_ \_**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — "статическая группа" брандмауэр

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**\_Проверка наличия \_ \_ доменных \_ сетей FW**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Проверка доменных сетей брандмауэра

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**\_Проверка наличия \_ \_ частных \_ сетей FW**  
Текст, отображаемый в элементе управления диалогового окна настройки брандмауэра — проверка частных сетей брандмауэра

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**\_Проверка наличия \_ \_ общедоступных \_ сетей FW**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра". Проверка общедоступных сетей брандмауэра

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**\_Настройка кнопки \_ IDC**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — кнопка Настройка

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**\_Отмена настройки \_ идентификатора**  
Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Конфигурация Отмена

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**\_ \_ \_ не \_ настроено FW для текста идентификаторов**  
Текст, отображаемый в диалоговом окне "Настройка брандмауэра-текст", брандмауэр не настроен

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**\_настроенное притекание текста идентификаторов \_ \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — текст настройки брандмауэра

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**\_ \_ имя правила брандмауэра идентификаторов \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — имя правила брандмауэра

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**\_ \_ Описание правила брандмауэра идентификаторов \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — описание правила брандмауэра

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_статический \_ заголовок ID**  
Текст, отображаемый в статическом заголовке диалогового окна настройки брандмауэра

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_название конфигурации идентификаторов \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — название конфигурации

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**\_заголовок статического \_ FW \_ ID**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — статический заголовок брандмауэра

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**\_встроенное по ID статической \_ GROUPBOX \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — статический брандмауэр-группа

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**ИДЕНТИФИКАТОРы \_ Проверка \_ \_ доменных \_ сетей FW**  
Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте доменные сети брандмауэра.

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**Проверка ИДЕНТИФИКАТОРов \_ \_ \_ частные \_ сети FW**  
Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте частные сети брандмауэра.

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**ИД \_ Проверка \_ \_ общедоступных \_ сетей FW**  
Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте общедоступные сети брандмауэра.

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**\_Настройка кнопки идентификаторов \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — Буттом Конфитуре

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**\_Отмена настройки идентификаторов \_**  
Текст, отображаемый в диалоговом окне настройки брандмауэра — конфигурация Отмена

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ИДЕНТИФИКАТОРы \_ \_ сообщения каптуретултип \_ коресистем**  
идентификатор ресурса для строки "для записи кадров используйте кнопку" запись "в Visual Studio".

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**ИДЕНТИФИКАТОРы \_ \_ нет**  
Не используется.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ИДЕНТИФИКАТОРы \_ et \_ SESSIONSTART**  
Не используется.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ИДЕНТИФИКАТОРы \_ et \_ сессионенд**  
Не используется.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ИДЕНТИФИКАТОРы \_ et \_ процессстарт**  
Не используется.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ИДЕНТИФИКАТОРы \_ et \_ процессенд**  
Не используется.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ИДЕНТИФИКАТОРы \_ et \_ фрамебегин**  
Не используется.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ИДЕНТИФИКАТОРы \_ et \_ фраминд**  
Не используется.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ИДЕНТИФИКАТОРы \_ et \_ усеревентбегин**  
Не используется.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ИДЕНТИФИКАТОРы \_ et \_ усеревентенд**  
Не используется.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ИДЕНТИФИКАТОРы \_ et \_ усермаркер**  
Не используется.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ИДЕНТИФИКАТОРы, \_ \_ вызов et**  
Не используется.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ИДЕНТИФИКАТОРы \_ et \_ обжектпопулатион**  
Не используется.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ИДЕНТИФИКАТОРы \_ et \_ обжекткреатион**  
Не используется.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ИДЕНТИФИКАТОРы \_ et \_ каллсинк**  
Не используется.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**ИДЕНТИФИКАТОРы \_ \_ неизвестны**  
Не используется.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**ИДЕНТИФИКАТОРы \_ активируют \_ нет**  
Не используется.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ програмстарт**  
Не используется.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_кадр триггера идентификаторов \_**  
Не используется.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_время активации идентификаторов \_**  
Не используется.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ усермаркер**  
Не используется.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ бегинусеревент**  
Не используется.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ ендусеревент**  
Не используется.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ каптурефраме**  
Не используется.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ апикаптуре**  
Не используется.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ИДЕНТИФИКАТОРы \_ ошибки \_ каллдата**  
Не используется.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ИДЕНТИФИКАТОРы \_ ошибки \_ креатинглог**  
Не используется.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ИДЕНТИФИКАТОРы \_ ункновнкалл**  
Не используется.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**Идентификатор \_ предупреждения \_ об \_ изменении уровня компонента \_**  
Не используется.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_Частота состояния \_ идентификатора**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ disable \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**Идентификатор \_ Отключить \_ Совместимость**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**Идентификатор, \_ собирающий \_ стеки вызовов**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**Идентификатор \_ включить \_ сдкеррор \_**  

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



