---
description: Описание эквивалентов API-интерфейсов видео Direct3D 12 к предыдущим версиям.
ms.assetid: ''
title: Переход на технологии видео Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 4004c35c21d9d6c67c0af3f9413521cf845437cddbc2ce245c3da495ed3daca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777424"
---
# <a name="migrating-to-direct3d-12-video"></a>Переход на технологии видео Direct3D 12

В этой статье описываются API-интерфейсы видео Direct3D 12, которые используются для реализации функций, доступных в предыдущих версиях. В целях повышения производительности и удобства использования видео-функций с наивысшим приоритетом некоторые функции Direct3D 11 полностью или частично не поддерживаются в Direct3D 12. 

Обратите внимание, что несмотря на то, что большинство функций Direct3D 11 доступны в Direct3D 12, структура API изменилась, поэтому во многих случаях не существует однозначного сопоставления интерфейсов API между двумя наборами API. Приведенные ниже таблицы предназначены для указания наиболее подходящих API-интерфейсов в Direct3D 12 для каждого API-интерфейса Direct3D 11, но способ использования новых API-интерфейсов может значительно отличаться. Например:

- Для декодирования кадра видео API-интерфейсы видео Direct3D 11 используют вызовы [декодербегинфраме](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe), [жетдекодербуффер](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer), [субмитдекодербуфферс](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)и [декодерендфраме](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe). В Direct3D 12 используется единственный метод  [ID3D12VideoDecodeCommandList::D екодефраме](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe).
- Для обработки видео в Direct3D 11 предоставлены отдельные методы для установки различных значений конфигурации, таких как [видеопроцессорсетаутпутколорспаце](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) и [видеопроцессорсетаутпуталфафиллмоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode). В Direct3D 12 эти значения задаются при создании обработчика видео, при вызове [ID3D12VideoDevice:: креатевидеопроцессор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)или при обработке кадра с вызовом [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1).





## <a name="id3d11videocontext"></a>ID3D11VideoContext
Предоставляет функции видео устройства Direct3D 11, включая декодирование видео, обработку видео, защиту содержимого на основе GPU и шифрование и расшифровку видео. Эта функциональность частично реализована для Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [конфигуреаусентикатедчаннел](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) | Не реализовано |
| [декодербегинфраме](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)| [ID3D12VideoDecodeCommandList::D екодефраме](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe),  [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument), [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream), [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames) |
| [декодерендфраме](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) | [ID3D12VideoDecodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videodecodecommandlist) |
| [декодерекстенсион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decoderextension) | Не реализован. |
| [декриптионблт](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)  | Не реализован. |
| [енкриптионблт](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt) | Не реализован. |
| [финишсессионкэйрефреш](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh) | Не реализован. |
| [жетдекодербуффер](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) | Не реализован. Сжатые буферы управляются приложениями в Direct3D 12. |
| [жетенкриптионблткэй](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey) | Не реализован. | 
| [неготиатеаусентикатедчаннелкэйексчанже](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) | Не реализован. |
| [неготиатекриптосессионкэйексчанже](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) | Не реализован. |
| [куеряусентикатедчаннел](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel) | Не реализован. |
| [релеаседекодербуффер](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer) | Не реализован. Сжатые буферы управляются приложениями в Direct3D 12. |
| [стартсессионкэйрефреш](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh) | Не реализовано |
| [субмитдекодербуфферс](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) | [ID3D12VideoDecodeCommandList::D Екодефраме](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [видеопроцессорблт](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt) | [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) |
| [Видеопроцессоржетаутпуталфафиллмоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputalphafillmode) [видеопроцессорсетаутпуталфафиллмоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputalphafillmode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. алфафиллмоде](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Видеопроцессоржетаутпутбаккграундколор](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputbackgroundcolor) [видеопроцессорсетаутпутбаккграундколор](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputbackgroundcolor) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. BackgroundColor](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [Видеопроцессоржетаутпутколорспаце](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputcolorspace) [видеопроцессорсетаутпутколорспаце](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputcolorspace) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. колорспаце](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  |
| [Видеопроцессоржетаутпутконстриктион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputconstriction) [видеопроцессорсетаутпутконстриктион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputconstriction) | Не реализован. Программная поддержка DRM не поддерживается. |
| [Видеопроцессоржетаутпутекстенсион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputextension) [видеопроцессорсетаутпутекстенсион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputextension) | Не реализован. |
| [Видеопроцессоржетаутпутстереомоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputstereomode) [видеопроцессорсетаутпутстереомоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputstereomode) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. енаблестерео](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Видеопроцессоржетаутпуттаржетрект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetoutputtargetrect) [видеопроцессорсетаутпуттаржетрект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetoutputtargetrect) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS. таржетректангле](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments) |
| [Видеопроцессоржетстреамалфа](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamalpha) [видеопроцессорсетстреамалфа](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamalpha)  | [D3D12_VIDEO_PROCESS_ALPHA_BLENDING. Буквы](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending) |
| [Видеопроцессоржетстреамаутопроцессингмоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamautoprocessingmode) [видеопроцессорсетстреамаутопроцессингмоде](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamautoprocessingmode) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. енаблеаутопроцессинг](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамколорспаце](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamcolorspace) [видеопроцессорсетстреамколорспаце](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamcolorspace) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. колорспаце](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамдестрект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamdestrect) [видеопроцессорсетстреамдестрект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamdestrect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. дестинатионректангле](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамекстенсион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamextension) [видеопроцессорсетстреамекстенсион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamextension) | Не реализован. |
| [Видеопроцессоржетстреамфилтер](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamfilter) [видеопроцессорсетстреамфилтер](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. филтерфлагс](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамфрамеформат](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamframeformat) [видеопроцессорсетстреамфрамеформат](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamframeformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Формат](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамлумакэй](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamlumakey) [видеопроцессорсетстреамлумакэй](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamlumakey) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. лумакэй](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреамаутпутрате](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamoutputrate) [видеопроцессорсетстреамаутпутрате](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamoutputrate) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. Частота](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Видеопроцессоржетстреампалетте](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampalette) [видеопроцессорсетстреампалетте](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampalette) | Не реализовано |
| [Видеопроцессоржетстреампикселаспектратио](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreampixelaspectratio) [видеопроцессорсетстреампикселаспектратио](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreampixelaspectratio) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Преобразует](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Видеопроцессоржетстреамротатион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamrotation) [видеопроцессорсетстреамротатион](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamrotation) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Преобразует](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Видеопроцессоржетстреамсаурцерект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamsourcerect) [видеопроцессорсетстреамсаурцерект](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamsourcerect) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Преобразует](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |
| [Видеопроцессоржетстреамстереоформат](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorgetstreamstereoformat) [видеопроцессорсетстреамстереоформат](/windows/win32/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamstereoformat) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Преобразует](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videocontext1"></a>ID3D11VideoContext1

Предоставляет расширенные функции видео устройства Direct3D 11, включая аппаратную DRM, улучшения использования поверхности, дополнительные функции обработки видео. Эта функция реализована для Direct3D 12 через новые интерфейсы.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| чекккриптосессионстатус | Подлежит уточнению | 
| [декодеренабледовнсамплинг](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [декодерупдатедовнсамплинг](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling) | [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) |
| [жетдатафорневхардварекэй](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-getdatafornewhardwarekey) | Подлежит уточнению |
| [SubmitDecoderBuffers1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-submitdecoderbuffers1) | [ID3D12VideoDecodeCommandList::D Екодефраме](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-decodeframe) |
| [видеопроцессоржетбехавиорхинтс](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetbehaviorhints) | Подлежит уточнению |
| [VideoProcessorGetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputcolorspace1) [VideoProcessorSetOutputColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputcolorspace1) | [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC. колорспаце](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc) |
| [Видеопроцессоржетаутпутшадерусаже](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetoutputshaderusage) [видеопроцессорсетаутпутшадерусаже](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetoutputshaderusage) | Подлежит уточнению |
| [VideoProcessorGetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreamcolorspace1) [VideoProcessorSetStreamColorSpace1](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreamcolorspace1) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC. колорспаце](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc) |
| [Видеопроцессоржетстреаммиррор](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorgetstreammirror) [видеопроцессорсетстреаммиррор](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-videoprocessorsetstreammirror) | [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS. Преобразует](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments) |

## <a name="id3d11videodecoder"></a>ID3D11VideoDecoder

Представляет декодер видео с аппаратным ускорением для Direct3D 11. Это интерфейс-оболочка вокруг [ID3D11VideoContext](/windows/win32/api/d3d11/nn-d3d11-id3d11videocontext) , который предоставляет реальную функциональность декодирования. Для видео Direct3D 12 не существует эквивалентного API.


## <a name="id3d11videodecoderoutputview"></a>ID3D11VideoDecoderOutputView

Определяет выходные поверхности, к которым можно получить доступ во время декодирования видео. В Direct3D 12 интерфейс [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor) напрямую использует объекты [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) .

## <a name="id3d11videodevice"></a>ID3D11VideoDevice

Предоставляет возможности декодирования видео и обработки видео на устройстве Direct3D 11. Это Главная точка входа для создания устройства видеодекодера и сеанса шифрования, а также для обработки видео, возможностей, профилей и т. д. Эта функциональность частично реализована для Direct3D 12.


| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [чекккриптокэйексчанже](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) | Не реализован. |
| [чекквидеодекодерформат](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) | [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [креатеаусентикатедчаннел](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) | Не реализован. |
| [креатекриптосессион](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) | Не реализован. |
| [креатевидеодекодер](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) | [ID3D12VideoDevice:: креатевидеодекодер](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder)  [ID3D12VideoDevice:: креатевидеодекодерхеап](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) |
| [креатевидеодекодераутпутвиев](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [креатевидеопроцессор](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor) | [ID3D12VideoDevice:: Креатевидеопроцессор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor)  |
| [креатевидеопроцессоренумератор](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator) | н/д |
| [креатевидеопроцессоринпутвиев](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [креатевидеопроцессораутпутвиев](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessoroutputview) | [ID3D12Texture2D](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) |
| [жетконтентпротектионкапс](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps) | Подлежит уточнению
| [жетвидеодекодерконфиг](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) | В Direct3D 12 поддерживается только режим ВЛД. [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats) |
| [жетвидеодекодерконфигкаунт](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) | н/д |
| [жетвидеодекодерпрофиле](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [жетвидеодекодерпрофилекаунт](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) | [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES. профилекаунт](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles) |
| [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedata) | [ID3D12Object:: Сетприватедата](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) |
| [SetPrivateDataInterface](/windows/win32/api/d3d11/nf-d3d11-id3d11videodevice-setprivatedatainterface) | [ID3D12Object:: Сетприватедатаинтерфаце](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface) |

## <a name="id3d11videodevice1"></a>ID3D11VideoDevice1

Обеспечивает расширенные возможности декодирования и видеообработки видео на устройстве Direct3D 11, включая дополнительные расширения, аппаратный DRM, декодирование, возможности видеодекодера и т. д. Эта функция реализована для Direct3D 12.

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [чекквидеодекодердовнсамплинг](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-checkvideodecoderdownsampling) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [жеткриптосессионприватедатасизе](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize) | Подлежит уточнению |
| [жетвидеодекодеркапс](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |
| [рекоммендвидеодекодердовнсамплепараметерс](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-recommendvideodecoderdownsampleparameters) | [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support) |


## <a name="id3d11videoprocessor"></a>ID3D11VideoProcessor

Представляет обработчик видео для Direct3D 11. Эта функция реализована для Direct3D 12 в [ID3D12VideoProcessor](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoprocessor)

| Direct3D 11 | Direct3D 12 |
|-------------|----------------|
| [жетконтентдеск](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getcontentdesc)| Не реализовано |
| [жетратеконверсионкапс](/windows/win32/api/d3d11/nf-d3d11-id3d11videoprocessor-getrateconversioncaps) | Не реализовано |


## <a name="id3d11videoprocessorenumerator-and-id3d11videoprocessorenumerator1"></a>ID3D11VideoProcessorEnumerator и ID3D11VideoProcessorEnumerator1

Перечисляет возможности видеопроцессора устройства Direct3D 11.
В Direct3D 12 функции перечисления заменяются [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport). 

##  <a name="id3d11videoprocessorinputview"></a>ID3D11VideoProcessorInputView

Определяет поверхности ввода, к которым можно получить доступ во время обработки видео.
В Direct3D 12 это заменяется на ID3D12Texture2D.

##  <a name="id3d11videoprocessoroutputview"></a>ID3D11VideoProcessorOutputView

Определяет выходные поверхности, к которым можно получить доступ во время обработки видео.
В Direct3D 12 это заменяется на ID3D12Texture2D.

## <a name="id3d11authenticatedchannel"></a>ID3D11AuthenticatedChannel

Обеспечивает безопасный канал связи с графическим драйвером или средой выполнения Microsoft Direct3D. Эта функция не реализована для видео Direct3D 12.

##  <a name="id3d11cryptosession"></a>ID3D11CryptoSession

Представляет сеанс шифрования. Используется для сценариев управления цифровыми правами программного обеспечения и оборудования. Для видео Direct3D 12 не существует эквивалентного открытого API.

## <a name="related-topics"></a>Связанные темы

[API-интерфейсы видео Direct3D 12](direct3d-12-video-apis.md)


 

 




