---
description: Определяет, является ли символ алфавитным или цифровым символом.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Функция Исчаралфанумерикврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452999"
---
# <a name="ischaralphanumericwrapw-function"></a>Функция Исчаралфанумерикврапв

\[**исчаралфанумерикврапв** доступен для использования в Windows XP. Он будет недоступен в последующих версиях. На своем месте следует использовать [**исчаралфанумерикв**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .\]

Определяет, является ли символ алфавитным или цифровым символом. Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.

> [!Note]  
> **Исчаралфанумерикврапв** — это оболочка для функции **исчаралфанумерикв** . Дополнительные сведения об использовании см. на странице [**исчаралфанумерик**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .

 

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*CH* \[ окне\]
</dt> <dd>

Тип: **WCHAR**

Проверяемый символ Юникода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

Если символ является буквенно-цифровым, возвращаемое значение не равно нулю.

Если символ не является буквенно-цифровым, возвращаемое значение равно нулю. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

**исчаралфанумерикврапв** предоставляет возможность использовать строки юникода в операционных системах, предшествующих Windows XP. Предпочтительным методом является использование [**исчаралфанумерикв**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Исчаралфанумерикврапв** должен вызываться напрямую из Shlwapi.dll с порядковым номером 28.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исчаралфанумерик**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
