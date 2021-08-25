---
title: Интерфейс Ивмтаскколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию объектов Task. Чтобы получить объект Ивмтаскколлектион, используйте свойство Tasks Ивмвиртуалпк.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Виртуальный ПК с интерфейсом Ивмтаскколлектион
- Ивмтаскколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958804"
---
# <a name="ivmtaskcollection-interface"></a>Интерфейс Ивмтаскколлектион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию объектов Task. Чтобы получить объект **ивмтаскколлектион** , используйте свойство [**Ивмвиртуалпк:: Tasks**](ivmvirtualpc-tasks.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмтаскколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмтаскколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **ивмтаскколлектион** имеет следующие свойства.



| Свойство                                                   | Тип доступа          | Описание                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                        |
| [**Count**](ivmtaskcollection-count.md)<br/>        | Только для чтения<br/> | Число задач в этой коллекции.<br/>                  |
| [**Компонент**](ivmtaskcollection-item.md)<br/>          | Только для чтения<br/> | Объект Task, соответствующий указанному индексу.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмтаскколлектион определен как 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмтаск**](ivmtask.md)
</dt> <dt>

[**Ивмвиртуалпк:: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

