---
description: Извлекает идентификатор кода ошибки (IDA) и неформатированную строку сообщения, если указана ошибка Jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Функция Жетеррравмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647953"
---
# <a name="jeterrrawmessage-function"></a>Функция Жетеррравмессаже

Извлекает идентификатор кода ошибки (IDA) и неформатированную строку сообщения, если указана ошибка Jet.

## <a name="syntax"></a>Синтаксис


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Err* 
</dt> <dd>

Ошибка Jet, соответствующая полученной информации.

</dd> <dt>

*пида* 
</dt> <dd>

Указатель на IDA.

</dd> <dt>

*пмессаже* 
</dt> <dd>

Указатель на сообщение об ошибке.

</dd> <dt>

*кбмессаже* 
</dt> <dd>

Число байтов в сообщении об ошибке.

</dd> <dt>

*пкбактуал* 
</dt> <dd>

Указатель на фактическое число считанных байтов.

</dd> <dt>

*пконтекстид* 
</dt> <dd>

Указатель на идентификатор контекста, связанный с файлом справки.

</dd> <dt>

*Пвсзелп/файл* 
</dt> <dd>

Указывает на указатель на файл, объясняющий ошибку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, она возвращает **Jet \_ еррсукцесс**; в противном случае она возвращает неформатированное сообщение об ошибке, указывающее конкретную причину сбоя.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
