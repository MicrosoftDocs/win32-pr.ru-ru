---
title: Константы TS_SS_ (Текстстор. h)
description: '\_ \_ Константы TS SS \, определенные до времени выполнения в \_ структуре состояния служб терминалов, описывают статические состояния документов.'
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681771"
---
# <a name="ts_ss_-constants"></a>\_ \_ \* Константы TS SS

\_ \_ \* Константы TS SS, определенные до времени выполнения в структуре [**\_ состояния служб терминалов**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , описывают статические состояния документов.



| Константа/значение                                                                                                                                                                                                                                                      | Описание                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_ СС \_ дисжоинтсел**</dt> <dt>(0x1)</dt> </dl>                             | Документ поддерживает несколько вариантов выбора.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_ \_Регионы SS**</dt> <dt>(0x2)</dt> </dl>                                         | Документ может содержать несколько регионов.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_ \_Транзитный СС**</dt> <dt>(0x4)</dt> </dl>                                | Предполагается, что документ будет иметь короткий цикл использования.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_ СС \_ нохиддентекст**</dt> <dt>(0x8)</dt> </dl>                          | Документ никогда не будет содержать скрытый текст.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_ СС \_ ткбаутокорректенабле**</dt> <dt>(0x10)</dt> </dl> | **Начиная с Windows 8:** Документ поддерживает автозамену, предоставляемую сенсорной клавиатурой.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_ СС \_ ткбпредиктионенабле**</dt> <dt>(0x20)</dt> </dl>    | **Начиная с Windows 8:** Документ поддерживает текстовые предложения, предоставляемые сенсорной клавиатурой.<br/> |



## <a name="remarks"></a>Комментарии

Элемент **двстатикфлагс** структуры **\_ состояния служб терминалов** использует эти константы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**TF \_ status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

