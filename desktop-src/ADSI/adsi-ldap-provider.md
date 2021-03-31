---
title: Поставщик LDAP ADSI
description: Поставщик LDAP ADSI реализует набор объектов ADSI, поддерживающих различные интерфейсы ADSI. Чтобы получить доступ к поставщику LDAP, выполните привязку к любому из объектов LDAP ADSI с помощью LDAP ADsPath.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Поставщик LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887596"
---
# <a name="adsi-ldap-provider"></a>Поставщик LDAP ADSI

Поставщик LDAP ADSI реализует набор объектов ADSI, поддерживающих различные интерфейсы ADSI. Чтобы получить доступ к поставщику LDAP, выполните привязку к любому из объектов LDAP ADSI с помощью LDAP ADsPath.

Для работы с поставщиком необходимо установить на клиентском компьютере Adsldp.dll, Adsldpc.dll, Adsmsext.dll и Activeds.dll.

> [!Note]  
> Поставщик LDAP по умолчанию (ADSI) не может считаться полностью потокобезопасным. Модули записи многопоточных приложений должны правильно координировать доступ между потоками посредством правильного использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.

 

 

 




