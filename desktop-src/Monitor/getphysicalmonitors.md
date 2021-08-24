---
title: Функция Жетфисикалмониторс
description: Возвращает физические мониторы, связанные с устройством вывода.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Настройка монитора функции Жетфисикалмониторс
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94cef0352aae75f95b1ff7ee9e65937f82c7b598a19cdce768028173dc97331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146157"
---
# <a name="getphysicalmonitors-function"></a>Функция Жетфисикалмониторс

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает физические мониторы, связанные с устройством вывода.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстрдевиценаме* \[ окне\]
</dt> <dd>

Указатель на [**\_ строковую структуру Юникода**](/windows/desktop/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*двфисикалмонитораррайсизе* \[ окне\]
</dt> <dd>

Число элементов в массиве *пдвнумфисикалмониторхандлесинаррай* . Чтобы получить требуемый размер массива, вызовите [**жетнумбероффисикалмониторс**](getnumberofphysicalmonitors.md).

</dd> <dt>

*пдвнумфисикалмониторхандлесинаррай* \[ заполняет\]
</dt> <dd>

Получает число элементов, которые функция копирует в массив *ффисикалмонитораррай* .

</dd> <dt>

*ффисикалмонитораррай* \[ заполняет\]
</dt> <dd>

Массив, который получает дескрипторы физических мониторов. Каждый обработчик должен быть освобожден путем вызова [**дестройфисикалмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Вместо использования этой функции приложения должны вызывать одну из следующих функций:

-   [**жетфисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Мониторинг функций конфигурации](monitor-configuration-functions.md)
</dt> </dl>

 

