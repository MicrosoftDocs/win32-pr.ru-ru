---
title: Поставщик ADSI WinNT
description: Поставщик Microsoft ADSI реализует набор объектов ADSI для поддержки различных интерфейсов ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI поставщика ADSI provider
- Служба WinNT Service Provider ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692794"
---
# <a name="adsi-winnt-provider"></a>Поставщик ADSI WinNT

Поставщик Microsoft ADSI реализует набор объектов ADSI для поддержки различных интерфейсов ADSI. имя пространства имен для поставщика Windows — "WinNT", а этот поставщик обычно называется поставщиком WinNT. Чтобы получить доступ к поставщику WinNT, выполните привязку к любому из [объектов ADSI в Winnt](adsi-objects-of-winnt.md), используя файл [WinNT AdsPath](winnt-adspath.md).

поставщик WinNT включен в компонент системы ADSI для Windows и Windows Server.

> [!Note]  
> Поставщик WinNT по умолчанию не может считаться полностью потокобезопасным. Средства записи многопоточных приложений должны обеспечивать обработку многопоточности для правильной координации любого доступа между потоками с помощью надлежащего использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.

 

 

 




