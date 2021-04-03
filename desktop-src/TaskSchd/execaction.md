---
title: Объект Ексекактион
description: Объект скрипта, представляющий действие, выполняющее операцию командной строки.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- выполнение планировщик задач действий, интерфейс
- планировщик задач объекта Ексекактион
- Планировщик задач объекта Ексекактион, описание
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137239"
---
# <a name="execaction-object"></a>Объект Ексекактион

Объект скрипта, представляющий действие, выполняющее операцию командной строки.

## <a name="members"></a>Элементы

Объект **ексекактион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **ексекактион** имеет следующие свойства.



| Свойство                                                            | Тип доступа           | Описание                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Аргументы**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Чтение/запись<br/> | Возвращает или задает аргументы, связанные с операцией командной строки.<br/>                                                 |
| [**Удостоверения**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Чтение/запись<br/> | Наследуется от объекта [**Action**](action.md) . Возвращает или задает идентификатор действия.<br/>                         |
| [**Путь**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Чтение/запись<br/> | Возвращает или задает путь к исполняемому файлу.<br/>                                                                           |
| [**Тип**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Только для чтения<br/>  | Наследуется от объекта [**Action**](action.md) . Возвращает тип действия.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Чтение/запись<br/> | Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.<br/> |



 

## <a name="remarks"></a>Комментарии

Если в свойствах [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)или [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) используются переменные среды, значения переменных среды кэшируются и используются при запуске Taskeng.exe (обработчик задач). Изменения переменных среды, происходящих после запуска обработчика задач, не будут использоваться обработчиком задач.

Это действие выполняет операцию командной строки. Например, действие может выполнить сценарий или запустить исполняемый файл.

При чтении или записи XML действие выполнения указывается в элементе [**exec**](taskschedulerschema-exec-actiongroup-element.md) схемы планировщик задач.

## <a name="examples"></a>Примеры

Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





