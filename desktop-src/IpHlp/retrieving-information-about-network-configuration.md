---
description: Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Получение сведений о конфигурации сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999405"
---
# <a name="retrieving-information-about-network-configuration"></a>Получение сведений о конфигурации сети

Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера. Чтобы получить общие сведения о конфигурации, используйте функцию [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Эта функция возвращает сведения, не относящиеся к конкретному адаптеру или интерфейсу. Например, **жетнетворкпарамс** возвращает список DNS-серверов, используемых локальным компьютером.

-   Примеры кода, включающие [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , см. [в разделе Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md).

 

 



