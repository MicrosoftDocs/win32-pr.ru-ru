---
description: Извлекает идентификатор кода ошибки (IDA) и создает окончательную строку вывода, когда предоставляется ошибка Jet и расширенные сведения об ошибке.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Функция Жетеррформаттедмессаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647945"
---
# <a name="jeterrformattedmessage-function"></a>Функция Жетеррформаттедмессаже

Извлекает идентификатор кода ошибки (IDA) и создает окончательную строку вывода, когда предоставляется ошибка Jet и расширенные сведения об ошибке.

## <a name="syntax"></a>Синтаксис


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
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

Номер ошибки Jet, используемый для поиска и форматирования отображаемого сообщения об ошибке.

</dd> <dt>

*пекстендедерроринфо* 
</dt> <dd>

Все сведения об ошибках Jet, включая имя базы данных, имя таблицы и любые незначительные сведения об ошибке.

</dd> <dt>

*пида* 
</dt> <dd>

Указатель на IDA, связанный с конкретным кодом ошибки.

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

Если функция выполнена успешно, она возвращает значение **Jet \_ еррсукцесс**; в противном случае возвращается отформатированное сообщение об ошибке, указывающее конкретную причину сбоя.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
