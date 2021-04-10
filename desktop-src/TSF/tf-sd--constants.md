---
title: Константы TF_SD_ (Мсктф. h)
description: '\_ \_ Константы TF SD \ описывают состояние документа.'
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135247"
---
# <a name="tf_sd_-constants"></a>\_ \_ \* Константы TF SD

\_ \_ \* Константы TF SD описывают состояние документа.



| Константа/значение                                                                                                                                                                                                                              | Описание                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**Tf \_ \_только SD ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt> </dl> | Документ доступен только для чтения и не может быть изменен.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**Tf \_ \_Загрузка SD**</dt> <dt>( \_ Загрузка SD служб терминалов \_ )</dt> </dl>     | Документ загружается и может быть неполным.<br/>    |



## <a name="remarks"></a>Комментарии

Элемент **двдинамикфлагс** структуры [ \_ состояния TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) использует эти константы.

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

[TF \_ status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[\_Константы SD служб терминалов \_ \*](ts-sd--constants.md)
</dt> <dt>

[Итфконтекстовнер::/Status](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[Итфконтекстовнерсервицес:: Онстатусчанже](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP::/Status](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[Итфстатуссунк:: Онстатусчанже](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

