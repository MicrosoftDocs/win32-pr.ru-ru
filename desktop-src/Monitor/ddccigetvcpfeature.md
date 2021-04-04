---
title: Функция ДдкЦижетвкпфеатуре
description: Возвращает текущее значение, максимальное значение и тип кода для монитора в виртуальной панели управления.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Настройка монитора функции ДдкЦижетвкпфеатуре
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988627"
---
# <a name="ddccigetvcpfeature-function"></a>Функция ДдкЦижетвкпфеатуре

> [!IMPORTANT]
> Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эту функцию.

 

Возвращает текущее значение, максимальное значение и тип кода для монитора в виртуальной панели управления.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмонитор* \[ окне\]
</dt> <dd>

Маркер физического монитора.

</dd> <dt>

*дввкпкоде* \[ окне\]
</dt> <dd>

Код, который необходимо запросить.

</dd> <dt>

*пвкт* \[ out, необязательно\]
</dt> <dd>

Получает тип кода перечислителя в виде члена перечисления [**\_ \_ \_ типа кода MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) -версии.

</dd> <dt>

*пдвкуррентвалуе* \[ заполняет\]
</dt> <dd>

Получает текущее значение кода "код версии + +".

</dd> <dt>

*пдвмаксимумвалуе* \[ out, необязательно\]
</dt> <dd>

Получает максимальное значение кода "код версии + +".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Комментарии

Приложения должны вызывать [**жетвкпфеатуреандвкпфеатуререпли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) вместо вызова этой функции.

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

 

