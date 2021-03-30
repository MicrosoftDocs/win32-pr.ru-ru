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
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997778"
---
# <a name="outputdebugstringwrapw-function"></a>Функция Аутпутдебугстрингврапв

\[Эта функция доступна для использования в Windows XP. Она может быть недоступна в последующих версиях. Используйте [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) на своем месте.\]

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

## <a name="remarks"></a>Примечания

**Аутпутдебугстрингврапв** предоставляет возможность использования строк Юникода в операционных системах до Windows XP. Предпочтительным методом является использование [**аутпутдебугстрингв**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Аутпутдебугстрингврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 115.

Если в приложении нет отладчика, системный отладчик отображает строку. Если в приложении нет отладчика, а системный отладчик неактивен, **аутпутдебугстрингврапв** не выполняет никаких действий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлвапип. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
