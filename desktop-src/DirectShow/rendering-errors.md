---
description: Ошибки отрисовки
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Ошибки отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495429"
---
# <a name="rendering-errors"></a>Ошибки отрисовки

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) определяет различные коды ошибок, используемые для регистрации ошибок отрисовки. Если проект не отображается правильно, модуль визуализации вызывает метод [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) . В следующей таблице перечислены параметры, заданные для **LogError**.

-   Код ошибки содержится в параметре *ErrorCode* .
-   Описание содержится в параметре ErrorString.
-   Описание содержится в параметре *ErrorString* .
-   При наличии дополнительной информации тип **Variant** содержится в элементе **VT** объекта **Variant** , на который указывает *пекстраинфо*.

> [!Note]  
> Описанные здесь коды ошибок не являются значениями **HRESULT** . Список возвращаемых значений **HRESULT** , характерных для DES, см. в разделе [коды ошибок и успешности](error-and-success-codes.md).

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Код ошибки</th>
<th>Описание</th>
<th>Дополнительные сведения</th>
<th>Тип Variant </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>Имя файла не существует, или DirectShow не распознает расширение файла.</td>
<td>Имя файла</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Тип файла не соответствует расширению файла, или файл поврежден.</td>
<td>Имя файла</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Имя файла является обязательным, но не было задано.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Не удается проанализировать источник данных, предоставленный этим источником.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Непредвиденная ошибка. Некоторые компоненты DirectShow установлены неправильно.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>Фильтр источника не принимает имена файлов.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>Тип носителя группы не поддерживается.</td>
<td>Номер группы</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Недопустимый номер потока для этого источника.</td>
<td>Номер потока</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Недостаточно памяти.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Одно растровое изображение в последовательности не совпадает с типом других.</td>
<td>Имя точечного рисунка</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Время воспроизведения клипа недопустимо, или последовательность независимых устройств (DIB) слишком мала.
<blockquote>
[!Note]<br />
При возникновении других ошибок отрисовки эта ошибка может возникать, несмотря на допустимость времени передачи.
</blockquote>
<br/></td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>Недопустимый идентификатор класса (CLSID) действия или перехода.</td>
<td>CLSID</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>Недопустимый идентификатор CLSID для действия по умолчанию или перехода.</td>
<td>CLSID</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Ваша версия DirectX не поддерживает трехмерные переходы.</td>
<td>CLSID</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Этот результат неверного типа или нарушен.</td>
<td>CLSID</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Такое свойство для объекта не существует.</td>
<td>Имя свойства</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Недопустимое значение для этого свойства.</td>
<td>Указанное значение</td>
<td><strong>ЗНАЧЕНИЕ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Синтаксическая ошибка в XML-файле.</td>
<td>Номер строки</td>
<td>VT_I4 (4-байтное целое число)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Не удалось найти фильтр, указанный в XML, по категории и экземпляру.</td>
<td>Понятное имя (экземпляр)</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Ошибка записи XML-файла на диск.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID не является допустимым фильтром звукового эффекты DirectShow.</td>
<td>CLSID</td>
<td><strong>ОСВОБОЖДАЕМОЙ</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Не удается найти программу сжатия для создания указанного формата сжатия.</td>
<td>Нет</td>
<td>Неприменимо</td>
</tr>
</tbody>
</table>



 

Следующие ошибки не должны возникать. Если возникла одна из этих ошибок, отправьте отчет об ошибках в корпорацию Майкрософт.



| Код ошибки                 | Описание                                 |
|----------------------------|---------------------------------------------|
| \_ \_ Анализ временной шкалы ИДЕНТИФИКАТОРов DEX \_  | Непредвиденная ошибка при синтаксическом анализе временной шкалы.      |
| \_ \_ Ошибка графа ИДЕНТИФИКАТОРов DEX \_     | Непредвиденная ошибка при построении графа фильтра. |
| \_Ошибка сетки идентификаторов DEX \_ \_      | Произошла непредвиденная ошибка во внутренней сетке.    |
| \_ \_ Ошибка интерфейса DEX \_ ID | Непредвиденная ошибка при получении интерфейса.      |



 

 

 




