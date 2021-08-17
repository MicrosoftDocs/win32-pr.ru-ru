---
title: Прочие константы хранилища текста (Текстстор. h)
description: В прочих константах хранилища текста задаются определенные свойства для хранилищ текста.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952102"
---
# <a name="miscellaneous-text-store-constants"></a>Прочие константы хранилища текста

В прочих константах хранилища текста задаются определенные свойства для хранилищ текста.



| Константа/значение                                                                                                                                                                                                                                           | Описание                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ \_Выбор по умолчанию**</dt> <dt>((ulong)-1)</dt> </dl> | Если для параметра *Улиндекс* [ITfContext::-SELECT](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) задано это значение, выбирается выбор по умолчанию.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ ЖЕА \_ Hidden**</dt> <dt>(0x1)</dt> </dl>                              | Если  для параметра dwFlags [итекстстореанчор:: onembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) задано это значение, то внедренный объект может находиться в скрытом тексте.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ ГТА \_ Hidden**</dt> <dt>(0x1)</dt> </dl>                              | Не используется.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ ST- \_ исправление**</dt> <dt>(0x1)</dt> </dl>                     | Если  для параметра dwFlags [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [Итекстстореанчор:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)или [ITextStoreACPSink:: онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) задано это значение, то текст представляет собой преобразование (исправление) существующего содержимого, а также все специальные сведения о текстовой разметке (метаданные), такие как данные файла WAV или идентификатор языка.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ \_Коррекция TC**</dt> <dt>(0x1)</dt> </dl>                     | Если  для параметра dwFlags [Итекстстореанчорсинк:: онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) задано это значение, то текст представляет собой преобразование (исправление) существующего содержимого, а также все специальные сведения о текстовой разметке (метаданные), такие как данные файла WAV или идентификатор языка.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ ВКУКИЕ \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                    | Используется внутри TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Распространяемые компоненты<br/>          | TSF 1,0 на Windows 2000 Professional<br/>                                         |
| Заголовок<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ITfContext:: выделять](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[Итекстстореанчор:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[Итекстстореанчор:: onembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink:: Онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[Итекстстореанчорсинк:: Онтекстчанже](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Различные константы платформы](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





