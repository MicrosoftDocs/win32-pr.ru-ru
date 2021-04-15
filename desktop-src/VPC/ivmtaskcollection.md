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
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415917"
---
# <a name="ivmtaskcollection-interface"></a>Интерфейс Ивмтаскколлектион

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет коллекцию объектов Task. Чтобы получить объект **ивмтаскколлектион** , используйте свойство [**Ивмвиртуалпк:: Tasks**](ivmvirtualpc-tasks.md) .

## <a name="members"></a>Элементы

Интерфейс **ивмтаскколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Ивмтаскколлектион** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **ивмтаскколлектион** имеет следующие свойства.



| Свойство                                                   | Тип доступа          | Описание                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Только для чтения<br/> | Перечислитель для коллекции.<br/>                        |
| [**Расчета**](ivmtaskcollection-count.md)<br/>        | Только для чтения<br/> | Число задач в этой коллекции.<br/>                  |
| [**Элемент**](ivmtaskcollection-item.md)<br/>          | Только для чтения<br/> | Объект Task, соответствующий указанному индексу.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмтаскколлектион определен как 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмтаск**](ivmtask.md)
</dt> <dt>

[**Ивмвиртуалпк:: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

