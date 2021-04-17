---
title: Функция ДдкЦижеткапабилитиесстринг
description: Возвращает строку, описывающую возможности монитора.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Настройка монитора функции ДдкЦижеткапабилитиесстринг
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661897"
---
# <a name="ddccigetcapabilitiesstring-function"></a>Функция ДдкЦижеткапабилитиесстринг

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает строку, описывающую возможности монитора.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Маркер физического монитора.

</dd> <dt>

*псзстринг* \[ заполняет\]
</dt> <dd>

Указатель на буфер, который получает строку возможностей. Чтобы получить длину строки возможностей, вызовите [**ддкЦижеткапабилитиесстрингленгс**](ddccigetcapabilitiesstringlength.md).

</dd> <dt>

*двленгс* \[ окне\]
</dt> <dd>

Размер буфера *псзстринг* в символах, включая завершающий символ null.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Комментарии

Приложения должны вызывать [**капабилитиесрекуестандкапабилитиесрепли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) вместо вызова этой функции.

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

 

