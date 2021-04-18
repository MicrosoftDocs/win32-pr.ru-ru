---
description: Освобождает \_ структуру контекста подписи, выделенную предыдущим вызовом функции сигнерсигнекс.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Функция Сигнерфрисигнерконтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663811"
---
# <a name="signerfreesignercontext-function"></a>Функция Сигнерфрисигнерконтекст

Функция **сигнерфрисигнерконтекст** освобождает структуру [**\_ контекста подписи**](signer-context.md) , выделенную предыдущим вызовом функции [**сигнерсигнекс**](signersignex.md) .

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псигнерконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста подписи**](signer-context.md) для освобождения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает значение S \_ ОК.

Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**контекст подписи \_**](signer-context.md)
</dt> <dt>

[**сигнерсигнекс**](signersignex.md)
</dt> </dl>

 

 
