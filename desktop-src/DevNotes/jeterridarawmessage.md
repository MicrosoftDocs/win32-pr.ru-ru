---
description: Извлекает неформатированную строку сообщения, если указан идентификатор кода ошибки (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Функция Жетерридаравмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 39bd07b3ac75bed85ff26dd7f014420ebaca8be16d6f0195d40e9161c0905496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955763"
---
# <a name="jeterridarawmessage-function"></a>Функция Жетерридаравмессаже

Извлекает неформатированную строку сообщения, если указан идентификатор кода ошибки (IDA).

## <a name="syntax"></a>Синтаксис


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*IDA* 
</dt> <dd>

Число, сопоставляемое с конкретным кодом ошибки и отображаемое пользователю.

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

Указатель на указатель на файл, объясняющий ошибку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, она возвращает значение **Jet \_ еррсукцесс**; в противном случае возвращается неформатированное сообщение, указывающее конкретную причину сбоя.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
