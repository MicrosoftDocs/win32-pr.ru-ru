---
description: Поставщики оборудования реализуют интерфейсы Ивсспровидеркреатеснапшотсет и Ивсшардвареснапшотпровидер.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Разработка поставщиков оборудования VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032714"
---
# <a name="developing-vss-hardware-providers"></a>Разработка поставщиков оборудования VSS

Поставщики оборудования реализуют интерфейсы [**ивсспровидеркреатеснапшотсет**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) и [**ивсшардвареснапшотпровидер**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **Ивсспровидеркреатеснапшотсет** реализует виртуализацию состояния теневого копирования. **Ивсшардвареснапшотпровидер** работает с абстракцией LUN. Поставщики должны быть реализованы как внутрипроцессный COM-сервер. Поставщики используют специфические для поставщика механизмы (как правило, частные IOCTL) для взаимодействия с подсистемой хранения, создающей экземпляры LUN теневого копирования.

-   [Регистрация и загрузка поставщика теневого копирования](shadow-copy-provider-registration-and-loading.md)
-   [Создание теневых копий для поставщиков](shadow-copy-creation-for-providers.md)
-   [Взаимодействие и поведение поставщика оборудования](hardware-provider-interactions-and-behaviors.md)

 

 



