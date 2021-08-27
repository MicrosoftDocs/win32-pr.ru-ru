---
description: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982217"
---
# <a name="internal-script-command-renderer-filter"></a>Фильтр модуля подготовки отчетов для команды внутреннего скрипта

Получает команды сценария и отправляет их в приложение.

Этот фильтр принимает команды сценария в одном из двух форматов:

-   MEDIATYPE \_ Text: каждый пример носителя содержит текстовую строку ANSI.
-   MEDIATYPE \_ команду скрипта. Каждый пример носителя содержит две строки в Юникоде, заканчивающиеся нулем, сцепленные вместе. Первая строка описывает тип команды, а вторая — команду скрипта.

    Когда фильтр получает образец, он отправляет уведомление о событии [**EC \_ OLE \_**](ec-ole-event.md) . Первый параметр события — это **BSTR** с типом команды, или, `Text` Если используется формат MEDIATYPE \_ Text. Вторым параметром события является **BSTR** с командой скрипта. Приложение может получить событие и ответить на команду скрипта.

Пример использования этого фильтра см. в разделе [средство синтаксического анализа Sami (CC)](sami--cc--parser-filter.md).




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a> | 
| Типы носителей входных закрепления | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | Не применяются | 
| Интерфейсы выходного ПИН-кода | Не применяются | 
| Фильтровать CLSID | {48025243-2D39-11CE-875D-00608CB78066} | 
| CLSID страницы свойств | Нет страницы свойств | 
| Исполняемый объект | Quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



