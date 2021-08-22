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
ms.openlocfilehash: e3dd051819b70ae93b7c615d803e12134221d55ffbd464c60d5b9c41d983eb9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678584"
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



 

## <a name="remarks"></a>Remarks

библиотека импорта, содержащая интерфейс **иорпкдебугнотифи** , не включена в пакет средств разработки программного обеспечения (SDK) Microsoft Windows. Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этих методов через интерфейс **иорпкдебугнотифи** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Н/Д</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Н/Д</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

