---
title: Структура строки
description: Представляет организацию данных в ресурсе версии файла. Он содержит строку, описывающую конкретный аспект файла, например версию файла, уведомления об авторских правах или его товарные знаки.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Меню структуры строк и другие ресурсы
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776734"
---
# <a name="string-structure"></a>Структура строки

Представляет организацию данных в ресурсе версии файла. Он содержит строку, описывающую конкретный аспект файла, например версию файла, уведомления об авторских правах или его товарные знаки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Члены

<dl> <dt>

**вленгс**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Длина данной структуры **строки** в байтах.

</dd> <dt>

**ввалуеленгс**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Размер (в словах) элемента **value** .

</dd> <dt>

**wType**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Тип данных в ресурсе версии. Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.

</dd> <dt>

**сзкэй**
</dt> <dd>

Тип: **WCHAR**

</dd> <dd>

Произвольная строка в Юникоде. Элемент **сзкэй** может иметь одно или несколько из следующих значений. Эти значения являются рекомендациями.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Обсуждения**


</dt> <dd>

Элемент **value** содержит любые дополнительные сведения, которые должны отображаться в целях диагностики. Эта строка может иметь произвольную длину.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Название**


</dt> <dd>

Элемент **значение** определяет компанию, которая создала файл. Например, "Корпорация Майкрософт" или "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**филедескриптион**


</dt> <dd>

Элемент **value** описывает файл таким образом, чтобы его можно было представить пользователям. Эта строка может быть представлена в списке, когда пользователь выбирает файлы для установки. например, "драйвер клавиатуры для клавиатуры в стиле" или "Microsoft Word для Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

Элемент **value** определяет версию этого файла. Например, **значение** может быть "3.00 a" или "5,00. RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**интерналнаме**


</dt> <dd>

Член **value** определяет внутреннее имя файла, если оно существует. например, эта строка может содержать имя модуля для библиотеки DLL, имя виртуального устройства для Windows виртуального устройства или имя устройства для драйвера устройства MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**легалкопиригхт**


</dt> <dd>

Элемент **value** описывает все уведомления об авторских правах, товарные знаки и зарегистрированные товарные знаки, которые применяются к файлу. Это должен быть полный текст всех уведомлений, допустимых символов, сроки действия прав, номера товарных знаков и так далее. На английском языке эта строка должна иметь формат "© Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**легалтрадемаркс**


</dt> <dd>

Элемент **значение** описывает все товарные знаки и зарегистрированные товарные знаки, которые применяются к файлу. Это должен быть полный текст всех уведомлений, допустимых символов, номера товарных знаков и так далее. На русском языке эта строка должна быть в формате "Windows является товарным знаком корпорации Майкрософт".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**оригиналфиленаме**


</dt> <dd>

Элемент **value** определяет исходное имя файла, не включая путь. Это позволяет приложению определить, был ли файл переименован пользователем. Это имя может быть не в формате MS-DOS 8,3-Format, если файл относится только к файловой системе, отличной от FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**приватебуилд**


</dt> <dd>

Элемент **value** описывает, кем, где и почему была создана эта частная версия файла. Эта строка должна присутствовать только в том случае, если флаг **VS \_ FF \_ приватебуилд** установлен в элементе **двфилефлагс** структуры [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Например, **значение** может быть "построено с помощью интерфейса OSCAR в \\ OSCAR2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**


</dt> <dd>

Элемент **value** определяет имя продукта, с которым распространяется этот файл. Например, эта строка может иметь значение "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

Элемент **value** определяет версию продукта, с которым распространяется этот файл. Например, **значение** может быть "3.00 a" или "5,00. RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**спеЦиалбуилд**


</dt> <dd>

Элемент **value** описывает, чем эта версия файла отличается от обычной версии. Эта запись должна присутствовать только в том случае, если флаг **VS \_ FF \_ спеЦиалбуилд** установлен в элементе **двфилефлагс** структуры [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Например, **значение** может быть "частная сборка для проблем с мышью для решения Olivetti на компьютерах M250 и M250E".

</dd> </dl> </dd> <dt>

**Заполнение**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Столько нуля слов, сколько необходимо, чтобы вычислить **значение** элемента на 32-разрядной границе.

</dd> <dt>

**Значение**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Строка, завершающаяся нулем. Дополнительные сведения см. в описании члена **сзкэй** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины. эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых с Windows пакетом средств разработки программного обеспечения (SDK).

Структура **строки** может иметь значение **сзкэй** , например "CompanyName", и **значение** "Корпорация Майкрософт". Другая структура **строки** с тем же значением **Сзкэй** может содержать **значение** "Microsoft GmbH". Это может произойти, если вторая **строка** была связана со структурой [**STRINGTABLE**](stringtable.md) , **сзкэй** значение которой равно 040704B0, то есть немецкий/Unicode.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**стрингфилеинфо**](stringfileinfo.md)
</dt> <dt>

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о версии](version-information.md)
</dt> </dl>

 

 





