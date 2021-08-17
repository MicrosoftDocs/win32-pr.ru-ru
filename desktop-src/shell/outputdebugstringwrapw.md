---
description: Отправляет в отладчик строку в Юникоде для вывода.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Функция Аутпутдебугстрингврапв (Шлвапип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858793"
---
# <a name="outputdebugstringwrapw-function"></a>Функция Аутпутдебугстрингврапв

\[эта функция доступна для использования в Windows XP. Она может быть недоступна в последующих версиях. Используйте [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) на своем месте.\]

Отправляет в отладчик строку в Юникоде для вывода.

> [!Note]  
> **Аутпутдебугстрингврапв** — это оболочка для функции **аутпутдебугстрингв** . Дополнительные сведения об использовании см. на странице [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .

 

## <a name="syntax"></a>Синтаксис


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпаутпутстринг* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку в Юникоде, заканчивающуюся нулем и отображаемую.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

**аутпутдебугстрингврапв** предоставляет возможность использовать строки юникода в операционных системах до Windows XP. Предпочтительным методом является использование [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Аутпутдебугстрингврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 115.

Если в приложении нет отладчика, системный отладчик отображает строку. Если в приложении нет отладчика, а системный отладчик неактивен, **аутпутдебугстрингврапв** не выполняет никаких действий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлвапип. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
