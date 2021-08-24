---
description: Получает идентификатор локали для родительского элемента поддерживаемого языкового стандарта.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Функция ДовнлевелжетпарентлокалелЦид (Нлсдл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 64cefdf4cc2a2c522a8295ab44e1810f0364d706d378979637700a7a3b72343a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765444"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Функция ДовнлевелжетпарентлокалелЦид

Получает [идентификатор локали](locale-identifiers.md) для родительского элемента поддерживаемого языкового стандарта.

> [!Note]  
> эта функция используется только приложениями, работающими в операционных системах, предшествующих Windows Vista. Для его использования требуется загружаемый пакет. приложения, которые работают только в Windows Vista и более поздних версиях, должны вызывать [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) с *LCType* , установленным в [LOCALE \_ спарент](locale-sparent.md).

 

## <a name="syntax"></a>Синтаксис


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Языковой стандарт* \[ окне\]
</dt> <dd>

Идентификатор локали языкового стандарта, для которого необходимо получить родительский идентификатор локали. С помощью макроса [**макелЦид**](/windows/desktop/api/Winnt/nf-winnt-makelcid) можно создать идентификатор языкового стандарта или использовать одно из следующих предопределенных значений.

-   [ИНВАРИАНТный ЯЗЫКовой стандарт \_](locale-invariant.md)
-   [система языкового стандарта \_ \_ по умолчанию](locale-system-default.md)
-   [\_Пользовательская Национальная настройка \_ по умолчанию](locale-user-default.md)

**Windows Vista и более поздних версий:** Также поддерживаются следующие пользовательские идентификаторы языкового стандарта.

-   [Пользовательский ЯЗЫКовой стандарт \_ \_ по умолчанию](locale-custom-constants.md)
-   [Пользовательский пользовательский интерфейс языкового стандарта \_ \_ \_ по умолчанию](locale-custom-constants.md)
-   [Пользовательский ЯЗЫКовой стандарт не \_ \_ указан](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает родительский идентификатор локали в случае успеха или 0 в противном случае. Чтобы получить расширенные сведения об ошибке, приложение может вызвать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), которая может возвращать один из следующих кодов ошибок:

-   Ошибка \_ : недопустимый \_ параметр. Любое из значений параметров было недопустимым.

## <a name="remarks"></a>Remarks

Требуемый заголовочный файл и библиотека DLL являются частью скачивания "API сопоставления данных нижнего уровня Microsoft NLS", доступного в [центре загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Распространяемые компоненты<br/>          | api сопоставления данных нижнего уровня Microsoft NLS в Windows кспор Windows Vista<br/>     |
| Заголовок<br/>                   | <dl> <dt>Нлсдл. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка национальных языков](national-language-support.md)
</dt> <dt>

[Функции поддержки национальных языков](national-language-support-functions.md)
</dt> <dt>

[Сопоставление данных локали](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
