---
description: Жетпринтексекутиондата извлекает текущий контекст печати.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Функция Жетпринтексекутиондата (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971353"
---
# <a name="getprintexecutiondata-function"></a>Функция Жетпринтексекутиондата

**Жетпринтексекутиондата** извлекает текущий контекст печати.

> [!Note]  
> Эта функция предназначена для использования драйверами принтеров, которые выполняются в контексте диспетчера очереди печати.

 

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает адрес структуры [**\_ \_ данных выполнения печати**](print-execution-data.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция выполнена. в противном случае — **false**. Если возвращаемое значение равно **false**, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить состояние ошибки.

## <a name="remarks"></a>Remarks

драйверы принтера должны вызывать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) в модуле винспул. drv для получения адреса функции **жетпринтексекутиондата** , так как **жетпринтексекутиондата** не поддерживается в Windows Vista и более ранних версиях Windows.

**Жетпринтексекутиондата** не выполняется, только если значение *pData* равно **null**.

Значение элемента **клиентапппид** [**\_ \_ данных выполнения печати**](print-execution-data.md) имеет смысл только в том случае, если значение **context** является **\_ контекстом выполнения печати \_ \_ WOW64**. Если значение **context** не является **\_ контекстом выполнения вывода \_ \_ WOW64**, значение **клиентапппид** равно 0.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Винспул. drv</dt> </dl>                   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Функция**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**\_контекст выполнения \_ печати**](print-execution-context.md)
</dt> <dt>

[**Печать \_ \_ данных выполнения**](print-execution-data.md)
</dt> </dl>

 

