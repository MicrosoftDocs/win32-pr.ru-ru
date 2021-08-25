---
title: Международные правила для текста и шрифтов
description: Международные правила для текста и шрифтов
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eeeeaf59f777610603787c3b8e6ed248f36810d34fc2026466b72ca57a1883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935404"
---
# <a name="international-text-and-font-guidance"></a>Международные правила для текста и шрифтов

## <a name="affected-platforms"></a>Затронутые платформы

<dl> клиенты — Windows 8 \| Windows 8.1  
серверы — Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

начиная с версии Windows 2000, поддержка просмотра текста для новых сценариев была добавлена в каждый основной выпуск Windows. описания изменений, внесенных в каждый основной выпуск, можно найти в статье [поддержка скриптов и шрифтов для Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) статьи в [центре разработки Go Global](https://msdn.microsoft.com/goglobal/default).

Обратите внимание, что поддержка сценария может потребовать внесения определенных изменений в компоненты стека текста, а также изменения шрифтов. Windows операционная система имеет множество компонентов стека текста: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 и др. Предоставленные сведения относятся в основном к GDI и DirectWrite. он также применяется к платформам пользовательского интерфейса, таким как RichEdit или агенту подготовки отчетов MSHTML, используемому для Windows 8 приложений магазина и для отрисовки веб-содержимого, хотя эти компоненты могут демонстрировать определенные различия.

## <a name="best-practices"></a>Советы и рекомендации

**Типографские рекомендации для разработчиков**

Типография — это основа языка разработки Майкрософт. Каждый из принципов проектирования Майкрософт усиливает важность оформления. В первый раз разработчики приложений имеют набор платформ, поддерживающих расширенные типографские функции. перейдите к разделу [отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10)) , чтобы узнать, как использовать JavaScript и HTML для отображения и редактирования текста в приложениях Windows Store.

**Метрики шрифта**

Метрики шрифтов — это область определенного важности для разработчиков приложений. Файлы шрифтов содержат различные значения, связанные с вертикальными и горизонтальными метриками. Эти значения задокументированы в [спецификации OpenType](https://www.microsoft.com/typography/otspec/) , и они предоставляются с помощью различных интерфейсов API, которые находятся в [ \_ \_ структуре метрик шрифта дврите](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) и в [структуре текстметрик](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Ресурсы

-   [Поддержка скриптов и шрифтов для Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Центр разработки Go Global](https://msdn.microsoft.com/goglobal/default)
-   [Отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Спецификация OpenType](https://www.microsoft.com/typography/otspec/)
-   [\_ \_ Структура МЕТРИК шрифта дврите](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Структура ТЕКСТМЕТРИК](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 