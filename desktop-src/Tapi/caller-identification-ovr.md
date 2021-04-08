---
description: Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса. Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Идентификация звонящего
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911211"
---
# <a name="caller-identification"></a>Идентификация звонящего

Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса. Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.

Эта информация не всегда доступна немедленно. Приложение, желающее использовать эти сведения и проверило, что поставщик услуг поддерживает его, должен проверить несколько раз, прежде чем предположить, что информация недоступна.

Не все поставщики служб поддерживают использование этих сведений.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двкаллеридфлагс**, **двкаллеридсизе**, **двкаллеридоффсет**, **двкаллериднамесизе**, **dwCallerIDNameOffset** и **dwCallerIDAddressType** lpCallInfo *).*

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ каллеридаддресстипе** член [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ каллериднаме** и **CI \_ CALLERIDNAME** CALLINFO [**\_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
