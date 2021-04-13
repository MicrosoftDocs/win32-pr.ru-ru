---
title: Международные правила для текста и шрифтов
description: Международные правила для текста и шрифтов
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412980"
---
# <a name="international-text-and-font-guidance"></a>Международные правила для текста и шрифтов

## <a name="affected-platforms"></a>Затронутые платформы

<dl> Клиенты — Windows 8.1 Windows 8 \|  
Серверы — Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Описание

С момента выпуска Windows 2000 в каждом основном выпуске Windows была добавлена поддержка просмотра текста для новых сценариев. Описания изменений, внесенных в каждом основном выпуске, можно найти в статье [Поддержка скриптов и шрифтов для Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) в [центре разработки Go Global](https://msdn.microsoft.com/goglobal/default).

Обратите внимание, что поддержка сценария может потребовать внесения определенных изменений в компоненты стека текста, а также изменения шрифтов. В операционной системе Windows имеется множество компонентов стека текста: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 и др. Предоставленные сведения в основном относятся к GDI и DirectWrite. Он также применяется к платформам пользовательского интерфейса, таким как RichEdit или агенту подготовки отчетов MSHTML, используемому для приложений Магазина Windows 8 и для отрисовки веб-содержимого, хотя эти компоненты могут демонстрировать определенные различия.

## <a name="best-practices"></a>Рекомендации

**Типографские рекомендации для разработчиков**

Типография — это основа языка разработки Майкрософт. Каждый из принципов проектирования Майкрософт усиливает важность оформления. В первый раз разработчики приложений имеют набор платформ, поддерживающих расширенные типографские функции. Перейдите к разделу [Отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10)) , чтобы узнать, как использовать JavaScript и HTML для отображения и редактирования текста в приложениях для Магазина Windows.

**Метрики шрифта**

Метрики шрифтов — это область определенного важности для разработчиков приложений. Файлы шрифтов содержат различные значения, связанные с вертикальными и горизонтальными метриками. Эти значения задокументированы в [спецификации OpenType](https://www.microsoft.com/typography/otspec/) , и они предоставляются с помощью различных интерфейсов API, которые находятся в [ \_ \_ структуре метрик шрифта дврите](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) и в [структуре текстметрик](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Ресурсы

-   [Поддержка скриптов и шрифтов для Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Центр разработки Go Global](https://msdn.microsoft.com/goglobal/default)
-   [Отображение и редактирование текста](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Спецификация OpenType](https://www.microsoft.com/typography/otspec/)
-   [\_ \_ Структура МЕТРИК шрифта дврите](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Структура ТЕКСТМЕТРИК](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 