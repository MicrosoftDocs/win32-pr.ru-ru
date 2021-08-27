---
description: Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Получение сведений о конфигурации сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767bdf0ec8c316bc4998e50e06e6f1a88f92742adff88f11745fbbd80c0b26ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050324"
---
# <a name="retrieving-information-about-network-configuration"></a>Получение сведений о конфигурации сети

Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера. Чтобы получить общие сведения о конфигурации, используйте функцию [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Эта функция возвращает сведения, не относящиеся к конкретному адаптеру или интерфейсу. Например, **жетнетворкпарамс** возвращает список DNS-серверов, используемых локальным компьютером.

-   Примеры кода, включающие [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , см. [в разделе Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md).

 

 



