---
title: Свойство Ивмтаск (Впккоминтерфацес. h)
description: Определяет, может ли задача быть отменена.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- Свойство, которое доменяется Virtual PC
- Свойство, которое доменяется Virtual PC, интерфейс Ивмтаск
- Ивмтаск интерфейс Virtual PC, свойство, которое доменяется
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a8fd4bc6a4f24e5f87f14c0d4ae7d1e50a35b8e40d1456bbbaccca221009c7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973794"
---
# <a name="ivmtaskiscancelable-property"></a>Свойство Ивмтаск::, которое следует отменять

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет, может ли задача быть отменена.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## <a name="property-value"></a>Значение свойства

**Значение true** , если задачу можно отменить до завершения, и **false** в противном случае.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Значение параметра равно **null**.<br/>  |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмтаск**](ivmtask.md)
</dt> </dl>

 

