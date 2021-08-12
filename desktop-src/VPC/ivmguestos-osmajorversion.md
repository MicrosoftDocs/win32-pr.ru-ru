---
title: Свойство дочерний osmajorversion Ивмгуестос (Впккоминтерфацес. h)
description: Основной номер версии гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: c9be8b4e-15fe-402d-8396-30be6b065b73
keywords:
- Дочерний osmajorversion свойство Virtual PC
- Дочерний osmajorversion свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство дочерний osmajorversion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMajorVersion
- IVMGuestOS.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfabbf082893897066e05ef5b83a5598a91ee2d62eac5eb89c36543b26a76222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594040"
---
# <a name="ivmguestososmajorversion-property"></a>Свойство Ивмгуестос:: дочерний osmajorversion

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает основной номер версии гостевой операционной системы, работающей на виртуальной машине.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_OSMajorVersion(
  [out, retval] BSTR *majorVersion
);
```



## <a name="property-value"></a>Значение свойства

Основная версия.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                       | Значение                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                          | Операция выполнена успешно.<br/>                        |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                            | Параметр имеет **значение NULL**.<br/>                           |
| <dl> <dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt> </dl>               | Виртуальная машина не запущена.<br/>                               |
| <dl> <dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt> </dl> | Компоненты интеграции не установлены в этой виртуальной машине.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                    | Произошла непредвиденная ошибка.<br/>                    |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

