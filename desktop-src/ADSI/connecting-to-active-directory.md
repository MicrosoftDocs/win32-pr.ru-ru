---
title: Подключение к Active Directory
description: Существует несколько методов, используемых для доступа к Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Подключение к Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6afd5aa0edd8a4c4a87bae7cde6a135fc3467771eed2dbc0cb7673984040832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692012"
---
# <a name="connecting-to-active-directory"></a>Подключение к Active Directory

Существует несколько методов, используемых для доступа к Active Directory. Для доступа к Active Directory рекомендуется использовать API ADSI. ADSI реализует протокол LDAP для взаимодействия с Active Directory. В следующем примере кода показано, как получить доступ к Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Откроется поставщик LDAP и подготовится к получению данных. Подключение не устанавливается, пока не будут запрошены данные. При запросе данных ADSI с помощью службы локатора пытается найти оптимальный контроллер домена для подключения и установит соединение с сервером. Этот процесс называется бессерверной привязкой.

ADSI также позволяет указать имя сервера, которое будет использоваться для соединения.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



В другом сценарии может быть только известно имя домена, но не конкретное имя сервера. Опять же, ADSI позволяет указать доменное имя. в Windows 2000 имя домена представлено в виде DNS-имени. Например, если Джо Ворден, администратор сети, выбирает подключение с использованием доменного имени, он мог бы использовать следующий пример кода.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI будет подключаться к одному из контроллеров домена в домене fabrikam.com.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Привязка к Active Directory объектам](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




