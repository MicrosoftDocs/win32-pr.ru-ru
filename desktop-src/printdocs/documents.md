---
description: В этом разделе описываются технологии документов, поддерживаемые Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS-документы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96324014d00a2a9fc106347fbeafe9842dedd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703140"
---
# <a name="xps-documents"></a>XPS-документы

В этом разделе описываются технологии документов, поддерживаемые Microsoft Windows.

-   [Выбор технологии документов](#choosing-a-document-technology)
-   [В этом разделе](#in-this-section)
-   [Средства документов XPS](#xps-document-tools)
-   [См. также](#related-topics)


## <a name="choosing-a-document-technology"></a>Выбор технологии документов

Корпорация Майкрософт предоставляет несколько различных технологий документов для поддержки различных приложений для работы с документами:

-   **XPS и Опенкспс**

    XPS и Опенкспс поддерживаются в Windows 8 и более поздних версиях Windows. Чтобы определить правильный сценарий использования для XPS и Опенкспс, см. предыдущую схему. Дополнительные сведения об этих технологиях документов см. в [статье Спецификация Open XML Paper (опенкспс)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    В случае использования Опенкспс с Windows 8 и Windows Server 2012 поддержка предоставляется только через [API документа XPS](documents-xps.md) .

    Если необходимо выполнить преобразование между Microsoft XPS (МСКСПС) и Опенкспс, то корпорация Майкрософт предоставила средство (XPSConverter.exe), которое позволяет преобразовать документы МСКСПС в формат Опенкспс и наоборот. Средство входит в комплект Windows Driver Kit (WDK). Чтобы скачать WDK, см. статью [как получить WDK](/windows-hardware/drivers/download-the-wdk).

    Дополнительные сведения о Опенкспс и Windows 8 см. в разделе [Поддержка опенкспс в Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API документов XPS**

    API документов XPS — это собственный API Windows, поддерживающий OM-модель XPS. API документов XPS появился в Windows 7 и может использоваться в программах пользовательского режима и драйверах принтера XPSDrv.

    Дополнительные сведения см. в статье API документов XPS и [API цифровой подписи XPS](xps-digital-signatures.md).

    \*API документов XPS также поддерживается в Windows Vista с пакетом обновления 2 (SP2) с обновлением платформы для Windows Vista и Windows Server 2008 с пакетом обновления 2 (SP2) с помощью обновления платформы для Windows Server 2008. Дополнительные сведения об обновлении платформы для Windows Vista или обновления платформы для Windows Server 2008 см. в [статье обновление платформы для Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .

-   **.NET Framework**

    Платформа .NET Framework обеспечивает поддержку документов XPS для программ, управляемых в пользовательском режиме.

    Платформа .NET Framework 3,0 поддерживается в Windows XP с пакетом обновления 2 (SP2) и более поздними версиями клиентских операционных систем Windows, а также на Windows Server 2003 с пакетом обновления 2 (SP2) и более поздних версиях операционных систем Windows Server.

    Платформа .NET Framework 3,5 поддерживается в версиях клиентских операционных систем Windows XP и в Windows Server 2003 и более поздних версиях операционных систем Windows Server.

    > [!Note]  
    > Рекомендуется использовать платформа .NET Framework для создания документов XPS только в клиентских приложениях, а не в серверных приложениях, если приложение не будет периодически завершать работу, как если бы оно было клиентским приложением.

     

    Дополнительные сведения о поддержке документов в платформа .NET Framework см. в разделе [Windows Presentation Foundation документы](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Для работы с XPS-документами в программе Используйте собственный API документа XPS или платформа .NET Framework. одновременное использование обоих в одной программе не поддерживается.

 

## <a name="in-this-section"></a>в этом разделе

В этом разделе описаны собственные технологии документов Windows, поддерживаемые Microsoft Windows.



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API документов XPS](documents-xps.md)<br/>                   | Предоставляет надежный формат для электронной бумаги.<br/> API документа XPS, описанный в этом разделе, предоставляет программам и драйверам печати доступ к содержимому и метаданным документа XPS.<br/> |
| [API цифровой подписи XPS](xps-digital-signatures.md)<br/> | Включает подписывание документов, проверку удостоверения подписавшего и указывает, изменился ли документ XPS с момента подписания.<br/>                                                                          |
| [Глоссарий XPS-документов](xpsapi-glossary.md)<br/>           | Определения терминов, используемых [API документов XPS](documents-xps.md) и [API цифровой подписи XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Средства документов XPS

Доступны следующие средства для тестирования и устранения неполадок в файлах XPS-документов.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Проверяет соответствие файла спецификациям формата XML (XPS) и спецификации Open Packaging Conventions (OPC).

-   [кспсанализер](/windows-hardware/drivers/devtest/xpsanalyzer)

    Средство командной строки, которое анализирует файлы документов XPS на совместимость со спецификацией XPS 1,0.

-   [птконформ](/previous-versions/dd327476(v=msdn.10))

    Средство, проверяющее допустимость документов PrintTicket и PrintCapabilities.

## <a name="related-topics"></a>См. также

<dl> <dt>

[API печати XPS](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Упаковка](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Вывод на печать](./printdocs-printing.md)
</dt> <dt>
  
[Пример программы печати](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 

