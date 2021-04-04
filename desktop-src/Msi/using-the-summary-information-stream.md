---
description: В этом разделе описано, какие функции в API установщик Windows могут вызывать свойства потока сводных данных. Дополнительные сведения о потоке сводных данных и принципах работы с базами данных см. в разделе Общие сведения о потоке сводных данных.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Использование потока сводных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998558"
---
# <a name="using-the-summary-information-stream"></a>Использование потока сводных данных

В этом разделе описано, какие функции в API установщик Windows могут вызывать свойства потока сводных данных. Дополнительные сведения о потоке сводных данных и принципах работы с базами данных см. [в разделе Общие сведения о потоке сводных данных](about-the-summary-information-stream.md).

-   Важно помнить, что установщик содержит разные типы баз данных, а некоторые свойства потока сводных данных имеют разные значения для разных баз данных. Дополнительные сведения см. в разделе [описания свойств сводки](summary-property-descriptions.md).
-   При открытии базы данных в качестве выходных данных другой базы данных информационный поток выходной базы данных фактически является зеркальной базой данных, предназначенной только для чтения, и поэтому не может быть изменен. Кроме того, она не будет сохраняться в базе данных. Чтобы создать или изменить сводные данные для выходной базы данных, ее необходимо закрыть и повторно открыть.

Следующие шаги описывают использование функций потока сводных данных.

**Использование свойств потока сводных данных**

1.  Получите маркер базы данных, содержащей информационный поток сводки, вызвав функцию [**мсижетсуммаринформатион**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) .
2.  Вызовите функцию [**мсисуммаринфожетпропертикаунт**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) , чтобы получить количество существующих свойств.
3.  Вызовите функцию [**мсисуммаринфожетпроперти**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) , чтобы просмотреть одно свойство сводных данных.
4.  Вызов функции [**мсисуммаринфосетпроперти**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) для установки одного свойства
5.  Вызовите функцию [**мсисуммаринфоперсист**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) , чтобы сохранить сводную информацию.
6.  Вызовите функцию [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) , чтобы создать сводные данные для существующего преобразования.

[Orca.exe](orca-exe.md) и [Msiinfo.exe](msiinfo-exe.md) — это средства, которые можно использовать для изменения или вывода сводного информационного потока базы данных. Эти средства доступны только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

Можно также получить доступ к информационному потоку сводки с помощью следующих методов и свойств [интерфейса автоматизации](automation-interface.md)установщик Windows.

-   [**Суммаринфо. Property**](summaryinfo-summaryinfo.md)
-   [**Суммаринфо. Пропертикаунт**](summaryinfo-propertycount.md)
-   [**Суммаринфо. PERSISTED**](summaryinfo-persist.md)
-   [**Установщик. SummaryInformation**](installer-summaryinformation.md)
-   [**База данных. SummaryInformation**](database-summaryinformation.md)
-   [**База данных. Креатетрансформсуммаринфо**](database-createtransformsummaryinfo.md)

Файл WiSumInf.vbs VBScript предоставляется в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). Этот пример скрипта можно использовать для управления потоком сводных данных пакета установщик Windows. Дополнительные сведения о WiSumInf.vbs см. в разделе [Управление сводными сведениями](manage-summary-information.md).

 

 



