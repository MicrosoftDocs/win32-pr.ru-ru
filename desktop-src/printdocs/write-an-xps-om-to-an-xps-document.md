---
description: Описание процедуры записи содержимого объектной модели XPS в программу в файл документа XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Запись объектной модели XPS в документ XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265347"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Запись объектной модели XPS в документ XPS

Описание процедуры записи содержимого объектной модели XPS в программу в файл документа XPS.

Если программа содержит ОБЪЕКТную систему XPS, содержащую полный документ, программа может записать OM XPS в файл как документ XPS, вызвав метод [**вритетофиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) интерфейса [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .

Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Запись полнофункциональной модели XPS в документ XPS

После настройки содержимого объектной модели XPS можно сохранить объект XPS в файл как документ XPS, вызвав метод [**вритетофиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) интерфейса [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> При записи объектной модели XPS в файл или поток не создается автоматически эскиз для документа XPS. Чтобы создать эскиз документа XPS, используйте интерфейс [**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="incrementally-writing-an-xps-document"></a>Добавочная запись документа XPS

Интерфейс [**икспсомпаккажевритер**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) можно использовать для добавочной записи частей XPS-документа; Например, если элементы документа создаются или обрабатываются последовательно.

> [!Note]  
> При записи объектной модели XPS в файл или поток не создается автоматически эскиз для документа XPS. Чтобы создать эскиз документа XPS, используйте интерфейс [**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Печать OM-объекта XPS](print-an-xps-om.md)
</dt> <dt>

**Используется в этом разделе**
</dt> <dt>

[**иопкпартури**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**икспсомсумбнаилженератор**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Инициализация объектной модели XPS](xps-object-model-initialization.md)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
