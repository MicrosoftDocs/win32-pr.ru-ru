---
description: Интерфейс Ибитебуффер предназначен для чтения, записи и управления объектами потоков. Этот объект по сути является оболочкой для объекта IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Интерфейс Ибитебуффер (Скардссп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8f0aa81106629142efeec7e22bdb495bea853c3c689d6b55887a62f896d89d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417414"
---
# <a name="ibytebuffer-interface"></a>Интерфейс Ибитебуффер

\[Интерфейс **ибитебуффер** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]

Интерфейс **ибитебуффер** предназначен для чтения, записи и управления объектами потоков. Этот объект по сути является оболочкой для объекта **IStream** .

## <a name="members"></a>Элементы

Интерфейс **ибитебуффер** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ибитебуффер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибитебуффер** содержит следующие методы.



| Метод                                           | Описание                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Клонировать**](ibytebuffer-clone.md)               | Создает точную копию объекта **ибитебуффер** .<br/>                                                              |
| [**Фиксация**](ibytebuffer-commit.md)             | Фиксирует [*транзакцию*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Копирует байты в другой объект.<br/>                                                                |
| [**Инициализация**](ibytebuffer-initialize.md)     | Инициализирует объект **ибитебуффер** .<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Разрешает доступ к диапазону байтов.<br/>                                                          |
| [**Чтение**](ibytebuffer-read.md)                 | Считывает байты в память.<br/>                                                                       |
| [**Отменить**](ibytebuffer-revert.md)             | Отклоняет изменения с момента последнего вызова [**фиксации**](ibytebuffer-commit.md) .<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Изменяет указатель поиска.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Изменяет размер объекта-потока.<br/>                                                         |
| [**STAT**](ibytebuffer-stat.md)                 | Получает статистические сведения о потоке.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Удаляет ограничение доступа, установленное ранее [**LockRegion**](ibytebuffer-lockregion.md).<br/>     |
| [**Запись**](ibytebuffer-write.md)               | Записывает байты в поток.<br/>                                                                    |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скардссп. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардссп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

