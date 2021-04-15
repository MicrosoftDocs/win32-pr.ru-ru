---
description: Используется для настройки компонентов CAPICOM.
title: Объект параметров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689010"
---
# <a name="settings-object-cryptography"></a>Объект Settings (криптография)

\[Объект **параметров** доступен для использования в операционных системах, указанных в разделе требования.\]

Объект **параметров** используется для настройки компонентов CAPICOM.

## <a name="members"></a>Элементы

Объект **параметров** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **параметров** имеет следующие свойства.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Свойство</th>
<th style="text-align: left;">Тип доступа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>активедиректорисеарчлокатион</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Задает или получает расположение поиска Active Directory. По умолчанию начальное расположение не указано. Если расположение не указано, выполняется поиск в глобальном каталоге, а затем выполняется поиск по домену по умолчанию. Поиск определяет, опубликован ли атрибут сертификата пользователя в этом расположении.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>енаблепромптфорцертификатеуи</strong></a><br/></td>
<td style="text-align: left;">Чтение/запись<br/></td>
<td style="text-align: left;">Задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя. <br/>
<blockquote>
[!Note]<br />
Задание этого свойства не отключает предупреждения, которые генерируются до того, как использование закрытого ключа выполняется из веб-приложения.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Объект **параметров** может быть создан и защищен для создания скриптов. ProgID для объекта **параметров** — CAPICOM. Settings. 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 




