---
title: Свойство имени Ивмвиртуалпк (Впккоминтерфацес. h)
description: извлекает имя приложения Windows Virtual PC.
ms.assetid: d33af684-ecba-4177-9ef3-cf6dff5bee4d
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMVirtualPC.Name
- IVMVirtualPC.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b3a0ea30ab6e78e0180a33d3955e5141ec70a5d4f3bac09204aa2a133517c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591717"
---
# <a name="ivmvirtualpcname-property"></a>Свойство Ивмвиртуалпк:: Name

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

извлекает имя приложения Windows Virtual PC.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualPCName
);
```



## <a name="property-value"></a>Значение свойства

имя приложения Windows Virtual PC.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                           | Значение                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                              | Операция выполнена успешно.<br/>                                                        |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                                | Параметр имеет **значение NULL**.<br/>                                                           |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                        | Произошла непредвиденная ошибка.<br/>                                                    |
| <dl> <dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt> </dl> | Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалпк**](ivmvirtualpc.md)
</dt> </dl>

 

