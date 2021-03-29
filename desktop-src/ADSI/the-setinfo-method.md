---
title: Метод Сетинфо
description: Метод IADs Сетинфо сохраняет текущие значения свойств этого объекта Active Directory из кэша свойств в базовом хранилище каталога. Это аналогично сбросу буфера на диск.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- Сетинфо ADSI, использование
- свойства ADSI, сохранение текущих значений свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328347"
---
# <a name="the-setinfo-method"></a>Метод Сетинфо

Метод [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) сохраняет текущие значения свойств этого объекта Active Directory из кэша свойств в базовом хранилище каталога. Это аналогично сбросу буфера на диск.

[**Сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) обновляет объекты, уже существующие в каталоге, или создает новую запись каталога для вновь созданных объектов.

В момент вызова [**сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , если какие-либо значения кэша свойств были записаны с помощью управляющего кода [**путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) (например, свойство \_ AD \_ Update или свойства ADS), то \_ \_ соответствующие запросы передаются в базовую службу каталогов.

 

 




