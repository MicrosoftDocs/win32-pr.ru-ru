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
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023142"
---
# <a name="the-setinfo-method"></a>Метод Сетинфо

Метод [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) сохраняет текущие значения свойств этого объекта Active Directory из кэша свойств в базовом хранилище каталога. Это аналогично сбросу буфера на диск.

[**Сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) обновляет объекты, уже существующие в каталоге, или создает новую запись каталога для вновь созданных объектов.

В момент вызова [**сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , если какие-либо значения кэша свойств были записаны с помощью управляющего кода [**путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) (например, свойство \_ AD \_ Update или свойства ADS), то \_ \_ соответствующие запросы передаются в базовую службу каталогов.

 

 




