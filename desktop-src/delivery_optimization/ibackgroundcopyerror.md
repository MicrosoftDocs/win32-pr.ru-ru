---
title: Интерфейс Ибаккграундкоперрор (Deliveryoptimization. h)
description: Используйте интерфейс Ибаккграундкоперрор, чтобы определить причину ошибки, и если процесс перемещения может быть продолжен.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Интерфейс Ибаккграундкоперрор
- Интерфейс Ибаккграундкоперрор, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490263"
---
# <a name="ibackgroundcopyerror-interface"></a>Интерфейс Ибаккграундкоперрор

Используйте интерфейс **ибаккграундкоперрор** , чтобы определить причину ошибки, и если процесс перемещения может быть продолжен.

Создает объект Error только в том случае, если состояние задания — BG_JOB_STATE_ERROR или BG_JOB_STATE_TRANSIENT_ERROR. Не создает объект Error при сбое метода интерфейса **ибаккграундкопикскскскс** . Объект Error доступен до тех пор, пока не начнется передача данных (состояние задания меняется на BG_JOB_STATE_TRANSFERRING) для задания.

Чтобы получить объект **ибаккграундкоперрор** , вызовите метод [**использованием метода ibackgroundcopyjob::**](ibackgroundcopyjob-geterror.md) GetObject.

## <a name="members"></a>Элементы

Интерфейс **ибаккграундкоперрор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ибаккграундкоперрор** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибаккграундкоперрор** содержит следующие методы.



| Метод                                                   | Описание                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Ошибка**](ibackgroundcopyerror-geterror-method.md) | Извлекает код ошибки и определяет контекст, в котором произошла ошибка.<br/> |
| [**Файл.**](ibackgroundcopyerror-getfile-method.md)   | Извлекает указатель интерфейса на объект File, связанный с ошибкой.<br/>     |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: возникла ошибка**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: State**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**Ибаккграундкопикаллбакк:: Жоберрор**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

