---
title: Свойство Ивмвиртуалмачине дисплея (Впккоминтерфацес. h)
description: Извлекает экран видео для виртуальной машины.
ms.assetid: ca5a433d-4613-4b6d-9de7-d9c6a2038e38
keywords:
- Показать свойство Virtual PC
- Отобразить свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Интерфейс Ивмвиртуалмачине Virtual PC, свойство дисплея
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Display
- IVMVirtualMachine.get_Display
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de930f76b015f85c8dcd50ad1a55630b55e99bdc31f19e93d11a1679257a98c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471953"
---
# <a name="ivmvirtualmachinedisplay-property"></a>Ивмвиртуалмачине::D свойство воспроизведения

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает экран видео для виртуальной машины.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Display(
  [out, retval] IVMDisplay **display
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмдисплай**](ivmdisplay.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>     |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачине**](ivmvirtualmachine.md)
</dt> </dl>

 

