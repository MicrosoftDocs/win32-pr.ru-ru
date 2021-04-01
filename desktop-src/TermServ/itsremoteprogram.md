---
title: Интерфейс Итсремотепрограм
description: Включает методы для установки и получения режима RemoteApp и параметры запуска для программы RemoteApp, такие как путь к исполняемому файлу и рабочий каталог.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Итсремотепрограм
- Службы удаленных рабочих столов интерфейса Итсремотепрограм, описание
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071765"
---
# <a name="itsremoteprogram-interface"></a>Интерфейс Итсремотепрограм

Включает методы для установки и получения режима RemoteApp и параметры запуска для программы RemoteApp, такие как путь к исполняемому файлу и рабочий каталог.

## <a name="members"></a>Элементы

Интерфейс **итсремотепрограм** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Итсремотепрограм** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **итсремотепрограм** содержит следующие методы.



| Метод                                                            | Описание                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**серверстартпрограм**](itsremoteprogram-serverstartprogram.md) | Указывает программу RemoteApp для запуска в удаленном сеансе.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **итсремотепрограм** имеет следующие свойства.



| Свойство                                                                   | Тип доступа           | Описание                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**ремотепрограммоде**](itsremoteprogram-remoteprogrammode.md)<br/> | Чтение/запись<br/> | Режим RemoteApp.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ итсремотепрограм определен как FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

