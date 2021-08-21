---
description: Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса. Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Идентификация звонящего
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3e4e412af29664d5a3585ad783545c13991250db8c449901db07868ea8feb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870008"
---
# <a name="caller-identification"></a>Идентификация звонящего

Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса. Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.

Эта информация не всегда доступна немедленно. Приложение, желающее использовать эти сведения и проверило, что поставщик услуг поддерживает его, должен проверить несколько раз, прежде чем предположить, что информация недоступна.

Не все поставщики служб поддерживают использование этих сведений.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двкаллеридфлагс**, **двкаллеридсизе**, **двкаллеридоффсет**, **двкаллериднамесизе**, **dwCallerIDNameOffset** и **dwCallerIDAddressType** lpCallInfo *).*

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ каллеридаддресстипе** член [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ каллериднаме** и **CI \_ CALLERIDNAME** CALLINFO [**\_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
