---
title: Функция Жетфисикалмонитордескриптион
description: Возвращает описание физического монитора.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Настройка монитора функции Жетфисикалмонитордескриптион
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251c24db32271802b94bd2beb7a381cc9b3adb50dd97842203947ea6a6895583
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534894"
---
# <a name="getphysicalmonitordescription-function"></a>Функция Жетфисикалмонитордескриптион

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает описание физического монитора.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Маркер физического монитора.

</dd> <dt>

*двфисикалмонитордескриптионсизеинчарс* \[ окне\]
</dt> <dd>

Число символов в массиве *сзфисикалмонитордескриптион* .

</dd> <dt>

*сзфисикалмонитордескриптион* \[ заполняет\]
</dt> <dd>

Указатель на массив, который получает описание. Число элементов в массиве должно быть не меньше, чем **\_ \_ \_ размер описания физического монитора**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Вместо использования этой функции приложения должны вызывать одну из следующих функций:

-   [**жетфисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

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

 

