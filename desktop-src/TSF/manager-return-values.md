---
title: Возвращаемые значения диспетчера (Мсктф. h)
description: Платформа текстовых служб создает возвращаемые значения в диапазоне от 0xHHHH0200 до 0xHHHH0507. В следующей таблице передаются значения, возвращаемые диспетчером в алфавитном порядке.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535009"
---
# <a name="manager-return-values"></a>Возвращаемые значения диспетчера

Платформа текстовых служб создает возвращаемые значения в диапазоне от 0x *HHHH* 0200 до 0x *HHHH* 0507. В следующей таблице передаются значения, возвращаемые диспетчером в алфавитном порядке.

> [!Note]  
> Указанные описания не являются специфическими. значение возвращаемого значения может различаться в зависимости от метода, который вернул значение.

 



| Возвращаемый код и значение                                                                                                                                                                                                                                                   | Описание                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**Tf \_ E \_ уже \_ существует**</dt> <dt>0x80040506</dt> </dl>                   | Сохраненный ключ зарегистрирован.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**Tf \_ Структура \_ E \_ отклонила**</dt> <dt>0x80040508</dt> </dl> | Владелец контекста отклонил композицию.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**Tf \_ E \_ disconnected**</dt> <dt>0x80040504</dt> </dl>                          | Объект контекста не находится в стеке документов.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**Tf \_ E \_ емптиконтекст**</dt> <dt>0x80040509</dt> </dl>                          | Контекст пуст.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**Tf \_ \_Формат E**</dt> <dt>0x8004020a</dt> </dl>                                            | Владелец контекста не может управлять объектами типа, предоставленными параметром pDataObject.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**Tf \_ E \_ инвалидпоинт**</dt> <dt>0x80040207</dt> </dl>                          | Недопустимые координаты экрана.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**Tf \_ E \_ инвалидпос**</dt> <dt>0x80040200</dt> </dl>                                | Недопустимая символьная позиции.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**Tf \_ E \_ инвалидвиев**</dt> <dt>0x80040505</dt> </dl>                             | Недопустимое представление контекста.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**Tf \_ Электронная \_ 0x80040500 заблокирована**</dt> <dt></dt> </dl>                                            | Контекст уже заблокирован.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**Tf \_ E \_ НЕинтерфейсный**</dt> <dt>0x80040204</dt> </dl>                             | Объект не поддерживает запрошенный интерфейс.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**Tf \_ 0x80040206 \_ разметки E**</dt> <dt></dt> </dl>                                      | Макет текста не был вычислен.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**Tf \_ 0x80040201 "E \_ Lock**</dt> " <dt></dt> </dl>                                            | У вызывающего объекта нет необходимого типа документа.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**Tf \_ 0x80040202, \_ объект E**</dt> <dt></dt> </dl>                                      | В указанной позиции не существует внедренного объекта.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**Tf \_ E \_**</dt> <dt>0x80040503</dt> </dl>                                | Для указанной функции не существует поставщика функций.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**Tf \_ 0x80040205 по \_ выделению E**</dt> <dt></dt> </dl>                             | В контексте нет выделенных элементов.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**Tf \_ E \_**</dt> <dt>0x80040203</dt> </dl>                                   | Указанная служба не существует или не может быть создана.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**Tf \_ E \_ нотовнедранже**</dt> <dt>0x80040502</dt> </dl>                       | Диспетчер TSF не владеет диапазоном.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**Tf \_ \_Диапазон E \_ не \_ охвачен**</dt> <dt>0x80040507</dt> </dl>         | Диапазон не находится внутри активной композиции.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**Tf \_ 0x80040209 \_ только для чтения**</dt> <dt></dt> </dl>                                      | Контекст редактирования доступен только для чтения.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**Tf \_ E \_ стаккфулл**</dt> <dt>0x80040501</dt> </dl>                                   | Стек контекста заполнен.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**Tf \_ E \_ синхронный**</dt> <dt>0x80040208</dt> </dl>                             | Невозможно получить синхронную блокировку только для чтения.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**Tf \_ S \_ асинхронный**</dt> <dt>0x00040300</dt> </dl>                                               | Данные будут получены асинхронно.<br/>                                              |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



 

 





