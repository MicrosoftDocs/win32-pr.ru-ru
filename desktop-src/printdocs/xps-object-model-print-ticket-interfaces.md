---
description: Этот интерфейс Икспсомпринттиккетресаурце API документов XPS предоставляет доступ к существующему билету на печать, а также возможность создания билета на печать в OM-модели XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Интерфейсы билета на печать Operations Manager XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713337"
---
# <a name="xps-om-print-ticket-interfaces"></a>Интерфейсы билета на печать Operations Manager XPS

Этот интерфейс [**ИКСПСОМПРИНТТИККЕТРЕСАУРЦЕ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) API документов XPS предоставляет доступ к существующему билету на печать, а также возможность создания билета на печать в OM-модели XPS.

## <a name="print-ticket-resources"></a>Печать ресурсов билетов

Интерфейс [**икспсомпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) позволяет программе считывать содержимое существующего билета на печать путем вызова метода **жетпринттиккетресаурце** интерфейса, поддерживающего билет печати. Новые ресурсы билетов на печать можно добавить в часть документа путем вызова **сетпринттиккетресаурце**.

Существует три уровня билетов на печать, которые определяют область действия билета на печать. Уровни билетов на печать: уровень задания (пакета), уровень документа и уровень страницы. В следующей таблице показана связь между уровнем билета на печать, соответствующим интерфейсом модели XPS и методами, используемыми для доступа к ресурсу билета на печать.

| Уровень билета на печать | Интерфейс                                                | Метод Get                                                                      | Метод Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Задание                | [**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**жетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**сетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Документ           | [**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**жетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**сетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Страница               | [**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**жетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**сетпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Печать содержимого билетов

Доступ к содержимому существующего билета на печать может осуществляться путем считывания из потока, связанного с ресурсом. Метод [**WebMethod**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) интерфейса [**икспсомпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) возвращает указатель на поток только для чтения, содержащий XML-содержимое билета на печать. Формат содержимого билета на печать описывается в [спецификации схемы печати](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Новый ресурс билета на печать можно создать, создав новый интерфейс [**икспсомпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) . В потоке записывается допустимый XML-запрос на печать в формате, а для обнаружения части билета на печать создается URI части. Дополнительные сведения о содержимом допустимого билета на печать см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Поток и URI части передаются как параметры вызова [**сетконтент**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) для установки нового ресурса билета на печать, а ресурс запроса на печать добавляется в соответствующую часть документа путем вызова метода **сетпринттиккетресаурце** , показанного в предыдущей таблице.

## <a name="print-ticket-inheritance"></a>Наследование билетов на печать

Билеты на печать наследуют свойства билетов на печать с большей областью действия. Например, билет печати на уровне документа наследует свойства билета на печать на уровне задания, связанного с последовательностью документов документа. Аналогичным образом, билет печати на уровне страницы наследует свойства билета печати на уровне документа, связанного с документом страницы. В этом процессе наследования свойства, указанные в билете печати нижнего уровня, переопределяют соответствующие свойства, которые в противном случае были бы унаследованы от билета печати более высокого уровня.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Печать спецификации схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**икспсомдокумент**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**икспсомдокументсекуенце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**икспсомпажереференце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**икспсомпринттиккетресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



