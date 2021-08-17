---
description: Сохранение и восстановление объектов Двдстате
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Сохранение и восстановление объектов Двдстате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922851cce72f736364c1f1e66b24032586221ad9cb75494c7286fe962eb34403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982574"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Сохранение и восстановление объектов Двдстате

Объекты [**идвдстате**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) позволяют приложениям сохранять моментальные снимки сеанса пользователя, в том числе такие сведения, как текущее место на диске, родительский уровень просмотра, выбранные потоки аудио и субтитров и т. д. Это означает, что пользователи могут сохранить свое место на DVD-Video диске и смотреть их позже.

Приложения не могут создавать объекты Двдстате. Эти объекты создаются внутренне навигатором DVD, когда приложение вызывает [**IDvdInfo2::-State**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Объекты Двдстате предоставляют интерфейс [**идвдстате**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) , позволяющий приложениям запрашивать определенные сведения.

В примере приложения DVD функции **кдвдкоре:: ресторебукмарк** и **Кдвдкоре:: савебукмарк** показывают, как сохранять и извлекать объекты двдстате.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



