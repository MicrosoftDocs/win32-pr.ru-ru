---
description: Удаляет именованное значение из указанного раздела реестра в автономном кусте реестра.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Функция Орделетевалуе (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669157"
---
# <a name="ordeletevalue-function"></a>Функция Орделетевалуе

Удаляет именованное значение из указанного раздела реестра в автономном кусте реестра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обработчик* \[ окне\]
</dt> <dd>

Маркер открытого раздела реестра в автономном кусте реестра.

</dd> <dt>

*лпвалуенаме* \[ в необязательное\]
</dt> <dd>

Удаляемое значение реестра. Если этот параметр имеет **значение NULL** или является пустой строкой, то неименованное значение по умолчанию, заданное функцией [**орсетвалуе**](orsetvalue.md) , удаляется.

В именах значений регистр не учитывается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Автономная библиотека реестра Windows версии 1,0 или более поздней<br/>                      |
| Header<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**орсетвалуе**](orsetvalue.md)
</dt> </dl>

 

 
