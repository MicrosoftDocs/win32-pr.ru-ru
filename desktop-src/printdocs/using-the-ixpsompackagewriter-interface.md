---
description: Интерфейс Икспсомпаккажевритер создает файл документа XPS, в который приложения могут записывать содержимое интерфейсов Икспсомпаже OM модели XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Использование интерфейса Икспсомпаккажевритер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098706"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Использование интерфейса Икспсомпаккажевритер

Интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) создает файл документа XPS, в который приложения могут записывать содержимое интерфейсов [**ИКСПСОМПАЖЕ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) OM модели XPS. Интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) наиболее удобен, когда содержимое документа обрабатывается или создается последовательно. В отличие от методов [**вритетофиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) и [**вритетостреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) интерфейса [**Икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , для использования интерфейса **Икспсомпаккажевритер** не требуется использовать весь FixedDocument или FixedDocumentSequence.

## <a name="overview"></a>Обзор

Интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) записывает по одной странице за раз, начиная от первой страницы документа XPS до последнего. Интерфейс можно использовать для создания простых файлов документов XPS, а также сложных файлов документов XPS, содержащих более одного FixedDocument в FixedDocumentSequence. В сложных файлах документов XPS Фикседдокументс также создаются последовательно, начиная с первого FixedDocument в FixedDocumentSequence. Интерфейс **икспсомпаккажевритер** не поддерживает создание содержимого документа в случайном порядке. Используйте его, например, чтобы создать последовательный отчет или выполнить обработку в фильтре драйверов устройств, где содержимое документа подается в драйвер последовательно.

## <a name="terminology-review"></a>Проверка терминологии

*Файл документа XPS* — это пакет Open Packaging Conventions (OPC), который соответствует спецификации формата XML. Так что, технически, интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) создает *пакет OPC*, но это пакет OPC, который соответствует спецификации формата XML. По этой причине в обсуждении документов XPS термины « *документ XPS* » и « *пакет* » часто взаимозаменяемы.

*Пакет* , созданный интерфейсом [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) , будет содержать необходимые компоненты документа XPS: FixedDocumentSequence, хотя бы один FixedDocument и хотя бы одну FixedPage. FixedDocumentSequence создается при создании экземпляра интерфейса **икспсомпаккажевритер** . FixedDocument создается каждый раз, когда вызывается [**икспсомпаккажевритер:: стартневдокумент**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) , а FixedPage создается каждый раз, когда вызывается [**Икспсомпаккажевритер:: addPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) . Поскольку интерфейс записывает содержимое документа последовательно, метод **addPage** добавляет страницу к последнему созданному FixedDocument.

## <a name="using-the-ixpsompackagewriter-interface"></a>Использование интерфейса Икспсомпаккажевритер

В следующей процедуре описывается создание файла документа XPS с помощью интерфейса [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) . Процедура не описывает, как создать экземпляр интерфейса [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) и его содержимое. Дополнительные сведения о **икспсомпаже** и добавлении содержимого на страницу см. в разделе [интерфейсы страничной модели XPS](xps-object-model-page-interfaces.md) и разделы, перечисленные в статье см. также.

 **Создание документа**

1.  Создайте экземпляр интерфейса [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) .

    В пакете будет создано пустое FixedDocumentSequence.

    -   Чтобы создать документ XPS в файле, вызовите [**икспсомобжектфактори:: креатепаккажевритеронфиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Чтобы создать документ XPS в потоке, вызовите метод [**икспсомобжектфактори:: креатепаккажевритеронстреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Запустите новый документ в пакете, вызвав [**икспсомпаккажевритер:: стартневдокумент**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Перед добавлением страницы вызовите [**икспсомпаккажевритер:: стартневдокумент**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) , чтобы добавить FixedDocument в FixedDocumentSequence, созданный на шаге 1.

3.  Добавление содержимого.
    -   Чтобы добавить в документ новую FixedPage, вызовите метод [**икспсомпаккажевритер:: addPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), передав ему указатель на интерфейс [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , который содержит содержимое FixedPage, которое требуется добавить.
    -   Чтобы создать новый FixedDocument в FixedDocumentSequence, вызовите [**икспсомпаккажевритер:: стартневдокумент**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Закройте пакет и его содержимое, вызвав [**икспсомпаккажевритер:: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Дополнительные функции

Методы интерфейса [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) также поддерживают добавление ресурсов, эскизов и билетов на печать. Эти компоненты документов можно добавлять на уровнях Package, FixedDocumentSequence, FixedDocument и FixedPage. Дополнительные сведения об использовании этого интерфейса для печати см. [в разделе Printing a XPS OM](print-an-xps-om.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование API цифровых подписей XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Интерфейсы страницы OM XPS](xps-object-model-page-interfaces.md)
</dt> <dt>

[Навигация по OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Работа с холстом и визуальными интерфейсами в модели XPS](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Работа с интерфейсами Path в модели XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Работа с интерфейсами Text, Graphics и Image в XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Интерфейсы билета на печать Operations Manager XPS](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



