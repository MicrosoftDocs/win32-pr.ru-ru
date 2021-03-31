---
title: Привязка к Active Directory объектам
description: Прежде чем продолжить работу с этим сценарием, необходимо понять, как именуются объекты ADSI в Active Directory и как привязать их. Привязка объекта ADSI подключает объект к службе каталогов и позволяет получить доступ к методам объекта.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067333"
---
# <a name="binding-to-active-directory-objects"></a>Привязка к Active Directory объектам

Прежде чем продолжить работу с этим сценарием, необходимо понять, как именуются объекты ADSI в Active Directory и как привязать их. Привязка объекта ADSI подключает объект к службе каталогов и позволяет получить доступ к методам объекта.

## <a name="adspath"></a>Действитель

Объект ADSI однозначно идентифицируется его строкой привязки, которая также называется ADsPath. Путь ADsPath представляет собой сочетание программного идентификатора (progID) поставщика ADSI и различающегося имени (DN) объекта.

Вот формат ADsPath:

"progID://DN"

-   Погид — программный идентификатор поставщика ADSI, например LDAP или WinNT.

-   ://— отделяет идентификатор progID от DN.

-   DN — различающееся имя объекта ADSI, которое является полным путем к объекту, где путь состоит из относительных различающихся имен (Рднс).

RDN — это имя объекта без пути, которое является уникальным для объектов того же уровня. RDN состоит из идентификатора атрибута и значения, например "DC = Fabrikam", где DC — это атрибут, а Fabrikam — это значение. DC — это идентификатор атрибута RDN, который обозначает компонент домена.

Ниже приведен пример ADsPath:

"LDAP://ДК = Fabrikam, DC = com"

## <a name="binding-the-object"></a>Привязка объекта

Вот как можно привязать объект Domain в этом сценарии:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



При выполнении этого примера кода ADSI использует различающееся имя для определения объектов ADSI для привязки. После того как ADSI привязывает эти объекты, можно получить доступ к их методам. В предыдущем примере кода объект домена привязывается к [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Теперь можно использовать методы в таких интерфейсах, как [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**WHERE**](/windows/desktop/api/Iads/nf-iads-iads-put), [**CREATE**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)и [**мовехере**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

После привязки объекта домена можно напечатать некоторые его атрибуты:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Дополнительные сведения о параметре ADsPath см. в разделе [Строка привязки](binding-string.md). Дополнительные сведения о привязке см. [в разделе Привязка к объекту ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание подразделения](creating-an-organizational-unit.md)
</dt> </dl>

 

 




