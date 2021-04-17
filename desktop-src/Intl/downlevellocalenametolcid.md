---
description: Преобразует имя языкового стандарта в идентификатор локали, который может использоваться для получения сведений из операционной системы.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Функция ДовнлевеллокаленаметолЦид (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651118"
---
# <a name="downlevellocalenametolcid-function"></a>Функция ДовнлевеллокаленаметолЦид

Преобразует [имя языкового](locale-names.md) стандарта в [идентификатор локали](locale-identifiers.md) , который может использоваться для получения сведений из операционной системы.

> [!Note]  
> Эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista. Для его использования требуется загружаемый пакет. Приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) для получения идентификатора локали.

 

## <a name="syntax"></a>Синтаксис


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпнаме* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем и представляющую [имя локали](locale-names.md).

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Флаги, указывающие тип имени. По умолчанию используется \_ имя локали нижнего уровня \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор локали, соответствующий имени локали в случае успеха.

Функция возвращает 0, если она не выполнена. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   Ошибка \_ : недопустимые \_ флаги. Указаны недопустимые значения флагов.
-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Эта функция не поддерживает Нейтральные языковые стандарты. Эквивалентная функция [**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) поддерживает [пользовательские языковые стандарты](custom-locales.md), но только для Windows Vista и более поздних версий.

 

Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                |
| Распространяемые компоненты<br/>          | Интерфейсы API сопоставления данных нижнего уровня Microsoft NLS в Windows XP с пакетом обновления 2 (SP2) и Латерорвиндовс Vista<br/> |
| Header<br/>                   | <dl> <dt>Нлсдл. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка национальных языков](national-language-support.md)
</dt> <dt>

[Функции поддержки национальных языков](national-language-support-functions.md)
</dt> <dt>

[Сопоставление данных локали](mapping-locale-data.md)
</dt> <dt>

[**локаленаметолЦид**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
