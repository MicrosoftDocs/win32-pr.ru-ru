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
ms.openlocfilehash: 717464b1ba44593a9b36ccf26e5df248cb95df9bfa40a7786896c87041e246d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045294"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Windows Библиотека автономных разделов реестра версии 1,0 или более поздней<br/>                      |
| Заголовок<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**орсетвалуе**](orsetvalue.md)
</dt> </dl>

 

 
