---
title: Функция ДдкЦижеткапабилитиесстрингленгс
description: Возвращает длину строки возможностей для монитора.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Настройка монитора функции ДдкЦижеткапабилитиесстрингленгс
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd30aeb1e71d88b649478d0ecd1c3052dbbe32372909882f73ae77db6e4dbc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066614"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a>Функция ДдкЦижеткапабилитиесстрингленгс

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает длину строки возможностей для монитора.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Маркер физического монитора.

</dd> <dt>

*пдвленгс* \[ заполняет\]
</dt> <dd>

Получает длину строки возможностей в символах, включая завершающий символ null.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Приложения должны вызывать [**жеткапабилитиесстрингленгс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) вместо вызова этой функции.

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

 

