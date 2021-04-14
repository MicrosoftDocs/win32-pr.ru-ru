---
description: Предоставляет сведения о приостановке работы приложения.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Интерфейс Исуспендингоператион (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541655"
---
# <a name="isuspendingoperation-interface"></a>Интерфейс Исуспендингоператион

Предоставляет сведения о приостановке работы приложения.

## <a name="members"></a>Элементы

Интерфейс **исуспендингоператион** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Исуспендингоператион** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **исуспендингоператион** содержит следующие методы.



| Метод                                                  | Описание                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**РБП**](isuspendingoperation-getdeferral.md) | Запрашивает задержку операции приостановки выполнения приложения.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **исуспендингоператион** имеет следующие свойства.



| Свойство                                                     | Тип доступа           | Описание                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Крайний срок**](isuspendingoperation-deadline.md)<br/> | Чтение/запись<br/> | Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**исуспендингдеферрал**](isuspendingdeferral.md)
</dt> <dt>

[**исуспендинжевентаргс**](isuspendingeventargs.md)
</dt> </dl>

 

 
