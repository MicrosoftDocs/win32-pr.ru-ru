---
title: Константы TF_IAS_ (Мсктф. h)
description: '\_ \_ Константы TF IAS \ используются в качестве флагов битовых знаков в методах, которые вставляют текст или внедренные объекты в выделенном фрагменте или точке вставки.'
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681874"
---
# <a name="tf_ias_-constants"></a>TF \_ IAS \_ \* константы

\_ \_ \* Константы TF IAS используются в качестве флагов битовых знаков в методах, которые вставляют текст или внедренные объекты в выделенном фрагменте или точке вставки.



| Константа/значение                                                                                                                                                                                                                                                                       | Описание                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**Tf \_ \_НЕЗАПРОС IAS**</dt> <dt>(0x1)</dt> </dl>                                                       | Текст вставляется, а при выходе в качестве указателя на диапазон устанавливается **значение NULL** . Не может использоваться вместе с \_ \_ флагом TF IAS куерйонли.<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**Tf \_ IAS \_ куерйонли**</dt> <dt>(0x2)</dt> </dl>                                                 | Не выполняйте вставку. Вызывающий объект требует, чтобы был установлен только указатель на диапазон. Параметр не может использоваться вместе с \_ флагом "TF IAS- \_ запрос".<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**Tf \_ Служба \_ IAS \_ без \_ композиции по умолчанию**</dt> <dt>(0x80000000)</dt> </dl> | Если требуется композиция, TSF не создаст композицию по умолчанию. Вызывающий объект должен начать композицию в диапазоне.<br/>         |



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

[ITextStoreACP:: Инсертембеддедатселектион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP:: Инсерттекстатселектион](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[Итекстстореанчор:: Инсертембеддедатселектион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[Итекстстореанчор:: Инсерттекстатселектион](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[Итфинсертатселектион:: Инсертембеддедатселектион](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[Итфинсертатселектион:: Инсерттекстатселектион](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





