---
title: Параметр быстрой привязки для операций записи и изменения пакетной службы
description: Когда объект службы каталогов привязан к, ADSI создает COM-объект, представляющий указанный объект каталога.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Параметр быстрой привязки для пакетной операции записи и изменения ADSI
- ADSI ADSI, использование параметра быстрой привязки для операций пакетной записи и изменения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533500"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Параметр быстрой привязки для операций записи и изменения пакетной службы

Когда объект службы каталогов привязан к, ADSI создает COM-объект, представляющий указанный объект каталога. При привязке ADSI обычно извлекает атрибут **objectClass** , чтобы интерфейсы ADSI могли предоставлять COM-интерфейсы, подходящие для этого класса объекта. Например, объект пользователя будет предоставлять интерфейс [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) в дополнение к базовым интерфейсам ADSI, поддерживаемым для всех объектов. Для одной операции это не должно оказывать влияния на производительность. Однако, если выполняются операции пакетной обработки, требующие сотен или тысяч привязок при низком соединении, и эти операции записывают данные в службу каталогов, возможно, потребуется обмен полной поддержкой объектов для ускорения привязки. Это называется быстрой привязкой и выполняется путем указания флага **\_ быстрой \_ привязки ADS** при вызове [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .

Быстрое связывание имеет следующие ограничения.

-   Операцию привязки необходимо выполнить с помощью функции [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или метода [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Операция привязки переходит к серверу каталога один раз, а не дважды. ADSI не извлекает атрибут **objectClass** и, следовательно, предоставляет только базовые интерфейсы ADSI для объекта.
-   Для COM-объекта поддерживаются следующие интерфейсы:

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**иадсделетеопс**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Если метод [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) используется для привязки к дочерним объектам, то дочерний объект имеет те же характеристики быстрой привязки, что и родитель.
-   Существование объекта, с которым выполняется привязка, не проверяется во время операции привязки, поэтому последующие вызовы метода завершатся ошибкой, если объект не существует. По этой причине Быстрая привязка должна использоваться только для тех объектов, которые существуют, например, непосредственно после выполнения запроса, который возвращает отличительные имена объектов, к которым выполняется привязка.
-   Расширения ADSI предоставляются для объектов класса **Top**. Поэтому предоставляются только расширения для базовых интерфейсов ADSI, перечисленных выше.

 

 