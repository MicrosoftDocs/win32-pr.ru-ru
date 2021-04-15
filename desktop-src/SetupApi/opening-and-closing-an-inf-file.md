---
description: Прежде чем функции настройки смогут получить доступ к информации в INF-файле, необходимо открыть ее с помощью вызова функции Сетупопенинффиле. Эта функция возвращает маркер в INF-файл.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Открытие и закрытие INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545791"
---
# <a name="opening-and-closing-an-inf-file"></a>Открытие и закрытие INF-файла

Прежде чем функции настройки смогут получить доступ к информации в INF-файле, необходимо открыть ее с помощью вызова функции [**сетупопенинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) . Эта функция возвращает маркер в INF-файл.

Если вы не знакомы с именем INF-файла, который необходимо открыть, можно использовать функцию [**сетупжетинффилелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) для получения списка файлов INF в каталоге.

После открытия INF-файла к открытому INF-файлу можно добавить дополнительные INF-файлы с помощью функции [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) . Это функционально аналогично оператору include. Если последующие функции установки ссылаются на открытый INF-файл, они также смогут получить доступ к любой информации, хранящейся в добавленных файлах.

Если не указать INF-файл во время вызова функции [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **сетупопенаппендинффиле** добавляет файлы, заданные ключом **лайаутфиле** в разделе **Version** файла Open INF.

Если сведения в INF-файле больше не нужны, вызовите функцию [**сетупклосеинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) , чтобы освободить ресурсы, выделенные во время вызова [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



