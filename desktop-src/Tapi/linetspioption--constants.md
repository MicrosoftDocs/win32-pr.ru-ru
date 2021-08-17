---
description: '\_Константы линетспиоптион описывают поставщики услуг по заказам, которые должны быть вызваны.'
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Константы LINETSPIOPTION_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404863"
---
# <a name="linetspioption_-constants"></a>\_Константы линетспиоптион

**\_ Константы линетспиоптион** описывают поставщики услуг по заказам, которые должны быть вызваны.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**ЛИНЕТСПИОПТИОН \_ нонринтрант**
</dt> <dd> <dl> <dt>



TAPI должен по одному вызывать функции этого поставщика услуг; перед вызовом той же или другой функции в том же или другом потоке он должен ожидать от каждой функции возврата (но не для завершения асинхронных функций).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



 

 




