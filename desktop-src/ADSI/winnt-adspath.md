---
title: Файл WinNT ADsPath
description: В этом разделе содержатся примеры строк, используемых для файла WinNT ADsPath.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Служба WinNT Service Provider ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838374"
---
# <a name="winnt-adspath"></a>Файл WinNT ADsPath

Строка ADsPath для поставщика ADSI WinNT может быть одной из следующих форм:


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



Доменное имя может быть либо NETBIOS-именем, либо именем DNS.

Сервер — это имя определенного сервера в домене.

Путь — это путь к объекту, например "printserver1/Printer2".

Имя объекта — это имя определенного объекта.

Класс объекта — это имя класса именованного объекта. Одним из примеров такого использования может быть «WinNT://MyServer/JeffSmith,user». Указание имени класса может повысить производительность операции привязки.

 

 




