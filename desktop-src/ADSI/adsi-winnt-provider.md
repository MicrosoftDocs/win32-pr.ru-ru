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
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410607"
---
# <a name="adsi-winnt-provider"></a>Поставщик ADSI WinNT

Поставщик Microsoft ADSI реализует набор объектов ADSI для поддержки различных интерфейсов ADSI. Имя пространства имен для поставщика Windows — "WinNT", а этот поставщик обычно называется поставщиком WinNT. Чтобы получить доступ к поставщику WinNT, выполните привязку к любому из [объектов ADSI в Winnt](adsi-objects-of-winnt.md), используя файл [WinNT AdsPath](winnt-adspath.md).

Поставщик WinNT включен в системный компонент ADSI для Windows и Windows Server.

> [!Note]  
> Поставщик WinNT по умолчанию не может считаться полностью потокобезопасным. Средства записи многопоточных приложений должны обеспечивать обработку многопоточности для правильной координации любого доступа между потоками с помощью надлежащего использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.

 

 

 




