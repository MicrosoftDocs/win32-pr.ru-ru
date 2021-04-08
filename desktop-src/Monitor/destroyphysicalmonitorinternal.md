---
title: Функция Дестройфисикалмониторинтернал
description: Закрывает маркер физического монитора.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Настройка монитора функции Дестройфисикалмониторинтернал
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891878"
---
# <a name="destroyphysicalmonitorinternal-function"></a>Функция Дестройфисикалмониторинтернал

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Закрывает маркер физического монитора.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Маркер физического монитора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Комментарии

Приложения должны вызывать [**дестройфисикалмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) вместо вызова этой функции.

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Мониторинг функций конфигурации](monitor-configuration-functions.md)
</dt> </dl>

 

