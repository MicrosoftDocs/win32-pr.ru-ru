---
description: Поставщики оборудования реализуют интерфейсы Ивсспровидеркреатеснапшотсет и Ивсшардвареснапшотпровидер.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Разработка поставщиков оборудования VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272587"
---
# <a name="developing-vss-hardware-providers"></a>Разработка поставщиков оборудования VSS

Поставщики оборудования реализуют интерфейсы [**ивсспровидеркреатеснапшотсет**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) и [**ивсшардвареснапшотпровидер**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **Ивсспровидеркреатеснапшотсет** реализует виртуализацию состояния теневого копирования. **Ивсшардвареснапшотпровидер** работает с абстракцией LUN. Поставщики должны быть реализованы как внутрипроцессный COM-сервер. Поставщики используют специфические для поставщика механизмы (как правило, частные IOCTL) для взаимодействия с подсистемой хранения, создающей экземпляры LUN теневого копирования.

-   [Регистрация и загрузка поставщика теневого копирования](shadow-copy-provider-registration-and-loading.md)
-   [Создание теневых копий для поставщиков](shadow-copy-creation-for-providers.md)
-   [Взаимодействие и поведение поставщика оборудования](hardware-provider-interactions-and-behaviors.md)

 

 



