---
title: Приложение г, заметки для Visual Basic разработчиков
description: В этом разделе содержатся сведения о Microsoft Active Accessibility для разработчиков Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986420"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Приложение г. примечания для Visual Basic разработчиков

В этом разделе содержатся сведения о Microsoft Active Accessibility для разработчиков Microsoft Visual Basic.

Приложения, написанные на Visual Basic, являются клиентами Microsoft Active Accessibility. Они не предоставляют сведения о своих настраиваемых элементах пользовательского интерфейса, так как они не реализуют [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) или какой-либо другой интерфейс модели COM.

В этой документации используются имена C/C++ для свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; Однако имена Visual Basic похожи. Например, свойство [**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) будет называться **аккнаме** в приложении Visual Basic.

## <a name="in-this-section"></a>Содержание раздела

-   [Примечания к методу Visual Basic: Аккнаме](visual-basic-method-notes--accname.md)
-   [Примечания к методу Visual Basic: Акквалуе](visual-basic-method-notes--accvalue.md)
-   [Visual Basic примеров программ](visual-basic-sample-programs.md)

 

 




