---
description: Функция Асинкстрингтраце — завершает настройку буфера трассировки с необязательными полями для трассировок в стиле sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Функция Асинкстрингтраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: ac099b0b69c1417c428aefe04b8e6591f945545a2b69196da588ebce8de23f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076178"
---
# <a name="asyncstringtrace-function"></a>Функция Асинкстрингтраце

Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле **sprintf**.

## <a name="syntax"></a>Синтаксис


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

32-разрядный параметр трассировки, используемый для фильтрации на уровне приложения.

</dd> <dt>

*сзформат* 
</dt> <dd>

Строка, завершающаяся нулем, которая описывает формат трассировки.

</dd> <dt>

*Фломастер* 
</dt> <dd>

Маркер для функций **vsprintf** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает длину инструкции трассировки в байтах.

## <a name="remarks"></a>Remarks

Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.

Тип данных « **\_ список ва** » — это стандартный тип, который используется для хранения информации, необходимой для **\_ завершения** макросов «# **\_ arg** » и «ва». Дополнительные сведения см. в разделе [стандартные типы](/cpp/c-runtime-library/standard-types?view=vs-2019).

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

