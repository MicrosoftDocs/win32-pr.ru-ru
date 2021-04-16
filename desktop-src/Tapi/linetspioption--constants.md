---
description: '\_Константы линетспиоптион описывают поставщики услуг по заказам, которые должны быть вызваны.'
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Константы LINETSPIOPTION_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689468"
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
| Header<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



 

 




