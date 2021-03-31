---
description: Доступ к областям DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Доступ к областям DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895097"
---
# <a name="access-to-directdraw-surfaces"></a>Доступ к областям DirectDraw

Образцы объектов мультимедиа, предоставляемые VMR для вышестоящего фильтра, поддерживают интерфейс [**ивмрсурфаце**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Чтобы получить интерфейс, вызовите QueryInterface в интерфейсе [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) и укажите IID \_ ивмрсурфаце. Вышестоящий фильтр может использовать методы Ивмрсурфаце для доступа к поверхности, созданной с помощью VMR, и управления ей.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование VMR для разработчиков фильтров DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



