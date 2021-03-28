---
description: Расширяет объект Ишеллдиспатч с помощью ряда новых функциональных возможностей.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Объект IShellDispatch2 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984676"
---
# <a name="ishelldispatch2-object"></a>Объект IShellDispatch2

Расширяет объект [**ишеллдиспатч**](ishelldispatch.md) с помощью ряда новых функциональных возможностей.

> [!Note]  
> **IShellDispatch2** реализован и доступен через объект [**Shell**](shell.md) .

 

## <a name="members"></a>Элементы

Объект **IShellDispatch2** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Объект **IShellDispatch2** содержит эти методы.



| Метод                                                               | Описание                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**канстартстопсервице**](ishelldispatch2-canstartstopservice.md)   | Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.<br/>    |
| [**финдпринтер**](ishelldispatch2-findprinter.md)                   | Отображает диалоговое окно **Поиск принтера** .<br/>                               |
| [**жетсистеминформатион**](ishelldispatch2-getsysteminformation.md) | Возвращает сведения о системе.<br/>                                           |
| [**Ограниченный доступ**](ishelldispatch2-isrestricted.md)                 | Извлекает из реестра параметр ограничений группы.<br/>              |
| [**иссервицеруннинг**](ishelldispatch2-isservicerunning.md)         | Возвращает значение, указывающее, запущена ли определенная служба.<br/> |
| [**сервицестарт**](ishelldispatch2-servicestart.md)                 | Запускает именованную службу.<br/>                                                 |
| [**сервицестоп**](ishelldispatch2-servicestop.md)                   | Останавливает именованную службу.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Выполняет указанную операцию с указанным файлом.<br/>                     |
| [**шовбровсербар**](ishelldispatch2-showbrowserbar.md)             | Отображает панель браузера.<br/>                                                 |



 

## <a name="remarks"></a>Примечания

Обсуждение служб Windows см. в документации по [службам](../services/services.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Объект оболочки**](shell.md)
</dt> <dt>

[**ишеллдиспатч**](ishelldispatch.md)
</dt> </dl>

 

 
