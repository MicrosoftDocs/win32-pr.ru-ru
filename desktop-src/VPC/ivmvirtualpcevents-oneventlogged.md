---
title: Метод Ивмвиртуалпцевентс Оневентлогжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что Windows Virtual PC регистрирует событие.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Метод Оневентлогжед Virtual PC
- Метод Оневентлогжед Virtual PC, интерфейс Ивмвиртуалпцевентс
- Ивмвиртуалпцевентс интерфейс Virtual PC, метод Оневентлогжед
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534391"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Метод Ивмвиртуалпцевентс:: Оневентлогжед

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что Windows Virtual PC регистрирует событие.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*логмессажеид* \[ окне\]
</dt> <dd>

Идентификатор сообщения журнала событий, который был занесен в журнал.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод вызывается, когда Windows Virtual PC регистрирует сообщение в журнале событий Windows. Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалпцевент \_ евентлогжед** , исходящем от [**ивмвиртуалпк**](ivmvirtualpc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалпцевентс определяется как efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалпцевентс**](ivmvirtualpcevents.md)
</dt> </dl>

 

