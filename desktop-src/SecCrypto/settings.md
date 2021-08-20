---
description: Используется для настройки компонентов CAPICOM.
title: объект Параметры
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
ms.openlocfilehash: 30cd71bdff3361d14e5114007509ccc5db33540ae2d56a7f75c7c71eec0761da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974336"
---
# <a name="settings-object-cryptography"></a>объект Параметры (криптография)

\[объект **Параметры** доступен для использования в операционных системах, указанных в разделе требования.\]

объект **Параметры** используется для настройки компонентов CAPICOM.

## <a name="members"></a>Элементы

объект **Параметры** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

объект **Параметры** имеет следующие свойства.



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



 

## <a name="remarks"></a>Remarks

можно создать объект **Параметры** и обеспечить безопасность сценариев. ProgID для объекта **Параметры** — CAPICOM. Параметры. 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 




