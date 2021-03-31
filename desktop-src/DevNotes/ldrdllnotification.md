---
description: Функция обратного вызова уведомлений, указанная с помощью функции Лдррегистердллнотификатион.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Функция обратного вызова Лдрдллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895342"
---
# <a name="ldrdllnotification-callback-function"></a>Функция обратного вызова Лдрдллнотификатион

\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Функция обратного вызова уведомлений, указанная с помощью функции [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) . Загрузчик вызывает эту функцию при первой загрузке библиотеки DLL.

**Предупреждение:** Функция обратного вызова уведомлений не является опасной для вызова функций в любой библиотеке DLL.

## <a name="syntax"></a>Синтаксис


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нотификатионреасон* \[ окне\]
</dt> <dd>

Причина, по которой была вызвана функция обратного вызова уведомлений. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                        | Значение                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ \_Причина уведомления библиотеки DLL \_ \_ загружена**</dt> <dt>1</dt> </dl>       | Библиотека DLL загружена. Параметр *нотификатиондата* указывает на структуру **\_ \_ \_ \_ данных уведомления загруженной библиотеки DLL LDR** . <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ \_Причина уведомления \_ DLL \_ выгружена**</dt> <dt>2</dt> </dl> | Библиотека DLL выгружена. Параметр *нотификатиондата* указывает на структуру **\_ \_ \_ \_ данных невыгруженных уведомлений библиотеки DLL LDR** . <br/> |



 

</dd> <dt>

*Нотификатиондата* \[ окне\]
</dt> <dd>

Указатель на постоянное объединение **уведомлений LDR \_ DLL \_** , которое содержит данные уведомления. Это объединение имеет следующее определение:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

Структура **\_ \_ \_ \_ данных уведомления загруженной библиотеки DLL LDR** имеет следующее определение:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

Структура **\_ \_ \_ \_ данных уведомления для выгруженной DLL-библиотеки LDR** имеет следующее определение:

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Контекст* \[ в необязательное\]
</dt> <dd>

Указатель на данные контекста для функции обратного вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция обратного вызова не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция обратного вызова уведомлений вызывается до того, как будет выполнена динамическая компоновка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лдррегистердллнотификатион**](ldrregisterdllnotification.md)
</dt> <dt>

[**лдрунрегистердллнотификатион**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




