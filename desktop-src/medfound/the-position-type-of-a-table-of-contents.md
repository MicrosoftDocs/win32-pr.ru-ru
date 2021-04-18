---
description: Тип расположения оглавления
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Тип расположения оглавления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692788"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Тип расположения оглавления

Некоторые методы интерфейса [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) имеют параметр с именем *енумтокпостипе* , имеющий тип [**перечислимого \_ \_ типа торговых терминалов**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Этот параметр указывает позицию в файле мультимедиа, где хранится оглавление. Целью было то, что оглавление может храниться либо в заголовке файла, либо в тексте файла как объект верхнего уровня. Эта функция пока не реализована.

В настоящее время таблицы содержимого могут храниться только как объекты верхнего уровня, поэтому для параметра *енумтокпостипе* необходимо всегда задавать **TOC \_ \_ топлевелобжект**. Если для *енумтокпостипе* задано значение почтовых **\_ \_ головок**, метод возвратит **E \_ нотимпл**.

Следующие методы имеют параметр *енумтокпостипе* .

-   [**жеттоккаунт**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**жеттокбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**жеттокбитипе**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**аддток**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**ремоветокбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**ремоветокбитипе**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочное руководством по программированию синтаксического анализатора содержимого](toc-parser-programming-guide.md)
</dt> </dl>

 

 



