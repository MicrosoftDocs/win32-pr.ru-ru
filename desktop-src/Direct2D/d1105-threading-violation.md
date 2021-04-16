---
title: Нарушение потоков D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Потоковый интерфейс аренды был одновременно обращен к нескольким потокам.
keywords:
- Direct2D о нарушении потоков D1105
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105658172"
---
# <a name="d1105-threading-violation"></a>D1105: нарушение потоков

\[ *Интерфейсный* поток аренды \] был одновременно обращен к нескольким потокам.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Адрес интерфейса, доступ к которому осуществлялся несколькими потоками.

</dd> </dl> 




 

## <a name="possible-causes"></a>Возможные причины

Использование экземпляра объекта из одной и той же однопотоковой фабрики из двух разных потоков.

 

 




