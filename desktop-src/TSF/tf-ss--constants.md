---
title: Константы TF_SS_ (Мсктф. h)
description: '\_ \_ Константы TF SS \, определенные до времени выполнения в \_ структуре состояния TF, описывают статические состояния документов.'
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071728"
---
# <a name="tf_ss_-constants"></a>\_ \_ \* Константы TF SS

\_ \_ \* Константы TF SS, определенные до времени выполнения в структуре [**\_ состояния TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , описывают статические состояния документов.



| Константа/значение                                                                                                                                                                                                                                                                              | Описание                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**Tf \_ СС \_ дисжоинтсел**</dt> <dt>(TS \_ SS \_ дисжоинтсел)</dt> </dl>                                     | Документ поддерживает несколько вариантов выбора.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**Tf \_ \_регионы SS**</dt> <dt>( \_ регионы TS SS \_ )</dt> </dl>                                                     | Документ может содержать несколько регионов.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**Tf \_ \_транзитный СС**</dt> <dt>( \_ \_ транзитный шлюз TS SS)</dt> </dl>                                         | Предполагается, что документ будет иметь короткий цикл использования.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**Tf \_ СС \_ ткбаутокорректенабле**</dt> <dt>(TS \_ SS \_ ткбаутокорректенабле)</dt> </dl> | **Начиная с Windows 8:** Документ поддерживает автозамену, предоставляемую сенсорной клавиатурой.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**Tf \_ СС \_ ткбпредиктионенабле**</dt> <dt>(TS \_ SS \_ ткбпредиктионенабле)</dt> </dl>     | **Начиная с Windows 8:** Документ поддерживает текстовые предложения, предоставляемые сенсорной клавиатурой.<br/> |



## <a name="remarks"></a>Комментарии

Элемент **двстатикфлагс** \_ структуры состояния TF использует эти константы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TF \_ status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

