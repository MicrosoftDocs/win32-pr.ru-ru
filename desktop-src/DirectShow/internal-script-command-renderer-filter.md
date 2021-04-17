---
description: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537349"
---
# <a name="internal-script-command-renderer-filter"></a>Фильтр модуля подготовки отчетов для команды внутреннего скрипта

Получает команды сценария и отправляет их в приложение.

Этот фильтр принимает команды сценария в одном из двух форматов:

-   MEDIATYPE \_ Text: каждый пример носителя содержит текстовую строку ANSI.
-   MEDIATYPE \_ команду скрипта. Каждый пример носителя содержит две строки в Юникоде, заканчивающиеся нулем, сцепленные вместе. Первая строка описывает тип команды, а вторая — команду скрипта.

    Когда фильтр получает образец, он отправляет уведомление о событии [**EC \_ OLE \_**](ec-ole-event.md) . Первый параметр события — это **BSTR** с типом команды, или, `Text` Если используется формат MEDIATYPE \_ Text. Вторым параметром события является **BSTR** с командой скрипта. Приложение может получить событие и ответить на команду скрипта.

Пример использования этого фильтра см. в разделе [средство синтаксического анализа Sami (CC)](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Неприменимо</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



