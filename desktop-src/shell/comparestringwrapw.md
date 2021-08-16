---
description: Сравнивает две строки символов Юникода с использованием заданного языкового стандарта.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Функция Компарестрингврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861515"
---
# <a name="comparestringwrapw-function"></a>Функция Компарестрингврапв

\[**компарестрингврапв** доступен для использования в Windows XP. Он будет недоступен в последующих версиях. На своем месте следует использовать [**компарестрингв**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .\]

Сравнивает две строки символов Юникода с использованием заданного языкового стандарта.

> [!Note]  
> **Компарестрингврапв** — это оболочка для функции **компарестрингв** . Дополнительные замечания об использовании см. на странице [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .

 

## <a name="syntax"></a>Синтаксис


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Языковой стандарт* \[ окне\]
</dt> <dd>

Тип: **LCID**

Идентификатор локали, используемый для сравнения. Этот параметр может быть одним из следующих заранее определенных идентификаторов языкового стандарта или идентификатором локали, созданным в макросе [**макелЦид**](/windows/win32/api/winnt/nf-winnt-makelcid) .

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**система языкового стандарта \_ \_ по умолчанию**


</dt> <dd>

Язык системы по умолчанию.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Пользовательская Национальная настройка \_ по умолчанию**


</dt> <dd>

Языковой стандарт текущего пользователя по умолчанию.

</dd> </dl> </dd> <dt>

*двкмпфлагс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Флаги, указывающие, как функция сравнивает две строки. По умолчанию эти флаги не заданы. Задайте значение 0, чтобы получить поведение по умолчанию или любое сочетание следующих значений.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**НОРМа \_ IGNORECASE**


</dt> <dd>

Не учитывать регистр.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**НОРМа \_ игнореканатипе**


</dt> <dd>

Не различать символы хирагана и катакана. Соответствующие символы хирагана и катакана сравниваются как равные.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**НОРМа \_ игноренонспаце**


</dt> <dd>

Пропускать несамостоятельные символы.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**НОРМа \_ игноресимболс**


</dt> <dd>

Игнорировать символы.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**НОРМа \_ игноревидс**


</dt> <dd>

Не следует различать однобайтовые символы и один и тот же символ в виде двухбайтовых символов.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**Сортировать \_ стрингсорт**


</dt> <dd>

Считать знаки препинания такими же, как символы.

</dd> </dl> </dd> <dt>

*lpString1* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на первую строку Юникода для сравнения.

</dd> <dt>

*cchCount1* \[ окне\]
</dt> <dd>

Тип: **int**

Число символов в строке, на которое указывает параметр *lpString1* . Число не содержит завершающего нуль символа. Если этот параметр имеет отрицательное значение, предполагается, что строка завершается нулем, а длина вычисляется автоматически.

</dd> <dt>

*lpString2* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на вторую сравниваемую строку Юникода.

</dd> <dt>

*cchCount2* \[ окне\]
</dt> <dd>

Тип: **int**

Число символов в строке, на которое указывает параметр *lpString2* . Число не содержит завершающего нуль символа. Если этот параметр имеет отрицательное значение, предполагается, что строка завершается нулем, а длина вычисляется автоматически.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Если функция выполняется неудачно, возвращается нулевое значение. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** может возвращать один из следующих кодов ошибок.

-   Ошибка \_ недопустимых \_ флагов
-   Ошибка \_ недопустимого \_ параметра

Если функция выполнена, возвращаемое значение является одним из следующих значений. 

| Требование | Значение |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ меньше \_    | Строка, на которую указывает параметр *lpString1* , меньше в лексической величине, чем строка, на которую указывает параметр *lpString2* . |
| CSTR \_ равно         | Строка, на которую указывает *lpString1* , равна значению в лексической строке, на которую указывает *lpString2*.                              |
| CSTR \_ больше \_ | Строка, на которую указывает *lpString1* , больше в лексической величине, чем строка, на которую указывает *lpString2*                           |



 

## <a name="remarks"></a>Remarks

**Предупреждение системы безопасности:** Неправильное использование этой функции может привести к нарушению безопасности приложения. Строки, которые не сравниваются правильно, могут формировать недопустимые входные данные. Тестовые строки, чтобы убедиться, что они действительны, прежде чем использовать их и предоставить обработчики ошибок. Дополнительные сведения см. в разделе [вопросы безопасности: международные функции.](../intl/security-considerations--international-features.md)

Предпочтительным методом является использование [**компарестрингв**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Компарестрингврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 45.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нет</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
