---
description: Форматирует время в виде строки времени для указанного языкового стандарта.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: Функция Жеттимеформатврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 6a23a615030b357eec4e40bbd8d6bc4a210bc7115b7aec76b45d6999de49f52c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679120"
---
# <a name="gettimeformatwrapw-function"></a>Функция Жеттимеформатврапв

\[**жеттимеформатврапв** доступен для использования в Windows XP. Она может быть недоступна в последующих версиях. На своем месте следует использовать [**жеттимеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .\]

Форматирует время в виде строки времени для указанного языкового стандарта. Функция форматирует либо указанное время, либо локальное системное время.

> [!Note]  
> **Жеттимеформатврапв** — это оболочка для функции **жеттимеформатв** . Дополнительные сведения об использовании см. на странице [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

 

## <a name="syntax"></a>Синтаксис


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Языковой стандарт* \[ окне\]
</dt> <dd>

Тип: **LCID**

Задает языковой стандарт, для которого должна быть отформатирована строка времени. Если *пвзформат* имеет **значение NULL**, функция форматирует строку в соответствии с форматом времени для этого языкового стандарта. Если *пвзформат* не равно **null**, функция использует языковой стандарт только для сведений, не указанных в формате строки рисунка (например, метки времени языкового стандарта).

Этот параметр может быть идентификатором локали, созданным в макросе [**макелЦид**](/windows/win32/api/winnt/nf-winnt-makelcid) , или одним из следующих предопределенных значений.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**система языкового стандарта \_ \_ по умолчанию**


</dt> <dd>

Национальная настройка системы по умолчанию.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Пользовательская Национальная настройка \_ по умолчанию**


</dt> <dd>

Языковой стандарт пользователя по умолчанию.

</dd> </dl> </dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Задает различные параметры функции. Можно указать сочетание следующих значений.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**наусероверриде ЛОКАЛи \_**


</dt> <dd>

Если задано значение, функция форматирует строку, используя системный формат времени по умолчанию для указанного языкового стандарта. Если значение не задано, функция форматирует строку с использованием любых пользовательских переопределений в формате времени по умолчанию для языкового стандарта. Этот флаг можно установить, только если *пвзформат* имеет **значение NULL**.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**Использование языкового стандарта \_ \_ CP \_ ACP**


</dt> <dd>

Использует системную кодовую страницу ANSI для перевода строк вместо кодовой страницы языкового стандарта.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**ВРЕМЯ \_ номинутесорсекондс**


</dt> <dd>

Не использует минуты или секунды.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**ВРЕМЯ в \_ секунду**


</dt> <dd>

Не использует секунды.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**ВРЕМЯ \_ нотимемаркер**


</dt> <dd>

Не использует маркер времени.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**ВРЕМЯ \_ FORCE24HOURFORMAT**


</dt> <dd>

Всегда использует 24-часовой формат времени.

</dd> </dl> </dd> <dt>

*лптиме* \[ окне\]
</dt> <dd>

Тип: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \***

Указатель на структуру [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , которая содержит сведения о времени для форматирования. Если этот указатель равен **null**, функция использует текущее локальное системное время.

</dd> <dt>

*пвзформат* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на формат, используемый для формирования строки времени. Если *пвзформат* имеет **значение NULL**, функция использует формат времени для указанного языкового стандарта. Дополнительные сведения см. в разделе [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

</dd> <dt>

*пвзтиместр* \[ заполняет\]
</dt> <dd>

Тип: **LPWSTR**

Указатель на буфер, который получает отформатированную строку времени.

</dd> <dt>

*кчтиме* \[ окне\]
</dt> <dd>

Тип: **int**

Размер (в символах) буфера *пвзтиместр* . Если *кчтиме* равен нулю, функция возвращает количество символов, необходимых для хранения отформатированной строки времени, а буфер, на который указывает *пвзтиместр* , не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Если функция выполнена, возвращаемое значение — это число символов, записанных в буфер, на который указывает *пвзтиместр*. Если параметр *кчтиме* равен нулю, то возвращаемое значение является числом символов, необходимых для хранения форматируемой строки времени. Счетчик включает завершающий нуль символ.

Если функция выполняется неудачно, возвращается нулевое значение. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** может возвращать один из следующих кодов ошибок.

<dl> <dt>

**Ошибка \_ недостаточного \_ буфера**
</dt> <dt>

**Ошибка \_ недопустимых \_ флагов**
</dt> <dt>

**Ошибка \_ недопустимого \_ параметра**
</dt> </dl>

## <a name="remarks"></a>Remarks

**жеттимеформатврапв** предоставляет возможность использовать строки юникода в операционных системах, предшествующих Windows XP. Предпочтительным методом является использование [**жеттимеформатв**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Жеттимеформатврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 310.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
