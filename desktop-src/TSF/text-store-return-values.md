---
title: Возвращаемые значения хранилища текста (Текстстор. h)
description: Когда диспетчер документов обрабатывает текстовое хранилище, он возвращает значения в диапазоне от 0xHHHH0200 до 0xHHHH0300. В следующей таблице перечислены возвращаемые значения из хранилища текста в алфавитном порядке.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534787"
---
# <a name="text-store-return-values"></a>Возвращаемые значения хранилища текста

Когда диспетчер документов обрабатывает хранилище текста, он возвращает значения в диапазоне от 0x *HHHH* 0200 до 0x *HHHH* 0300. В следующей таблице перечислены возвращаемые значения из хранилища текста в алфавитном порядке.



| Возвращаемый код и значение                                                                                                                                                                                                                          | Описание                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_ \_Формат E**</dt> <dt>0x8004020a</dt> </dl>                   | Приложение не поддерживает тип данных, содержащийся в объекте [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) , для вставки с помощью [**ITextStoreACP:: инсертембеддед**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_ E \_ инвалидпоинт**</dt> <dt>0x80040207</dt> </dl> | Параметр не находится внутри ограничивающего прямоугольника любого символа.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_ E \_ инвалидпос**</dt> <dt>0x80040200</dt> </dl>       | Указанный диапазон расширяется за пределами документа.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_ E \_ НЕинтерфейсный**</dt> <dt>0x80040204</dt> </dl>    | Объект не поддерживает запрошенный интерфейс.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_ 0x80040206 \_ разметки E**</dt> <dt></dt> </dl>             | Приложение не вычислило макет текста.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_ 0x80040201 "E \_ Lock**</dt> " <dt></dt> </dl>                   | Приложение не имеет блокировки только для чтения или чтения и записи для документа.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_ 0x80040202, \_ объект E**</dt> <dt></dt> </dl>             | Перед внедренным символом TF char не размещается смещение внедренного содержимого \_ \_ .<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_ 0x80040205 по \_ выделению E**</dt> <dt></dt> </dl>    | Документ не имеет выделения.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_ E \_**</dt> <dt>0x80040203</dt> </dl>          | Содержимое не может быть возвращено в соответствие с идентификатором GUID службы.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_ 0x80040209 \_ только для чтения**</dt> <dt></dt> </dl>             | Документ доступен только для чтения. Невозможно изменить содержимое.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_ E \_ синхронный**</dt> <dt>0x00040300</dt> </dl>    | Документ не может быть заблокирован синхронно.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_ S \_ Async**</dt> <dt>(0x1)</dt> </dl>                         | Документ успешно получил асинхронную блокировку.<br/>                                                                                                                                              |



 

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

[**ITextStoreACP:: Инсертембеддед**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

