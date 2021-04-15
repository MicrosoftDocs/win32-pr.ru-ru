---
description: Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Функция Сетасинктрацепарамсекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648117"
---
# <a name="setasynctraceparamsex-function"></a>Функция Сетасинктрацепарамсекс

Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле **sprintf**.

## <a name="syntax"></a>Синтаксис


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзмодуле* 
</dt> <dd>

Имя модуля, связанного с трассировкой.

</dd> <dt>

*псзфиле* 
</dt> <dd>

Имя исходного файла, содержащего исключение.

</dd> <dt>

*ллине* 
</dt> <dd>

Номер строки исключения в исходном файле.

</dd> <dt>

*псзфунктион* 
</dt> <dd>

Имя функции для исключения.

</dd> <dt>

*двтрацемаск* 
</dt> <dd>

Константа флага трассировки, представляющая один из доступных типов трассировки. Этот параметр может принимать любое из следующих значений.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Неустранимая \_ Ошибка \_Маска трассировки** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Ошибка при \_ \_Маска трассировки** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Отладка \_ \_Маска трассировки** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Состояние \_ \_Маска трассировки** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Функция \_ Func \_Маска трассировки** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Сообщение об ошибке \_ \_Маска трассировки** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Все \_ \_Маска трассировки** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает значение 1, если функция выполнена. в противном случае возвращается значение 0.

## <a name="remarks"></a>Комментарии

Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
