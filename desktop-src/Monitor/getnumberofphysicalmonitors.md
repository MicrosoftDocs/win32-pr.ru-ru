---
title: Функция Жетнумбероффисикалмониторс
description: Возвращает число мониторов фикал, связанных с устройством вывода.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Настройка монитора функции Жетнумбероффисикалмониторс
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673ef12d1e02d87e068784408824bb78dbbbad5dfd5c907ece58c3eb7673e957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534934"
---
# <a name="getnumberofphysicalmonitors-function"></a>Функция Жетнумбероффисикалмониторс

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает число мониторов фикал, связанных с устройством вывода.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстрдевиценаме* \[ окне\]
</dt> <dd>

Указатель на [**\_ строковую структуру Юникода**](/windows/desktop/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*пдвнумбероффисикалмониторс* \[ заполняет\]
</dt> <dd>

Получает число физических мониторов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Вместо использования этой функции приложения должны вызывать одну из следующих функций:

-   [**жетнумбероффисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Мониторинг функций конфигурации](monitor-configuration-functions.md)
</dt> </dl>

 

