---
title: Интерфейс Иорпкдебугнотифи
description: Предоставляет функции удаленной отладки.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- COM интерфейса Иорпкдебугнотифи
- Интерфейс COM интерфейса Иорпкдебугнотифи, описание
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535441"
---
# <a name="iorpcdebugnotify-interface"></a>Интерфейс Иорпкдебугнотифи

Предоставляет функции удаленной отладки.

## <a name="when-to-implement"></a>Когда следует реализовывать

Реализуйте этот интерфейс, чтобы включить удаленную отладку через RPC.

## <a name="when-to-use"></a>Назначение

Этот интерфейс следует использовать для внутрипроцессного удаленной отладки, когда программные исключения не следует использовать для уведомлений отладчика COM. Он позволяет выполнять внутрипроцессный отладчики для получения уведомлений от прямых вызовов, использующих эти методы.

## <a name="members"></a>Элементы

Интерфейс **иорпкдебугнотифи** наследует от интерфейса [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . **Иорпкдебугнотифи** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иорпкдебугнотифи** содержит следующие методы.



| Метод                                                              | Описание                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md)       | Отправляет данные из клиентского отладчика в отладчик сервера.<br/>         |
| [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md) | Извлекает размер буфера RPC из клиентского отладчика.<br/>        |
| [**клиентнотифи**](iorpcdebugnotify-clientnotify.md)               | Информирует клиента о том, что исходящий запрос отладчика к серверу.<br/>   |
| [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md)       | Отправляет данные из отладчика сервера в клиентский отладчик.<br/>         |
| [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md) | Извлекает размер буфера RPC из отладчика на стороне сервера.<br/>        |
| [**сервернотифи**](iorpcdebugnotify-servernotify.md)               | Информирует сервер о входящем запросе отладчика от клиента.<br/> |



 

## <a name="remarks"></a>Комментарии

Библиотека импорта, содержащая интерфейс **иорпкдебугнотифи** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK). Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этих методов через интерфейс **иорпкдебугнотифи** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Н/Д</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Н/Д</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ОРПК \_ dbg \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**\_БУФЕР ОРПК dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_аргументы инициализации \_ ОРПК**](orpc-init-args.md)
</dt> <dt>

[**дллдебугобжектрпчук**](dlldebugobjectrpchook.md)
</dt> </dl>

 

