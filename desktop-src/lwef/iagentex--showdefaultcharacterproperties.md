---
title: Иажентекс Шовдефаултчарактерпропертиес
description: Иажентекс Шовдефаултчарактерпропертиес
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487692"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>Иажентекс:: Шовдефаултчарактерпропертиес

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Отображает окно свойств символов по умолчанию.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Координата x окна в пикселях относительно начала координат экрана (вверху слева).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*&*
</dt> <dd>

Координата по оси y окна в пикселях относительно начала координат экрана (вверху слева).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*буседефаулт*
</dt> <dd>

Флаг расположения по умолчанию. Если этот параметр имеет **значение true**, то Microsoft Agent отображает окно страницы свойств для символа по умолчанию в последнем расположении.

> [!Note]  
> Для Windows 2000 может потребоваться вызвать новый API [**алловсетфореграундвиндов**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) , чтобы это окно стало передним планом. Дополнительные сведения о настройке окна переднего плана в Windows 2000 см. в документации по пакету SDK для платформы.

 

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентнотифисинкекс::D Ефаултчарактерчанже**](iagentnotifysinkex--defaultcharacterchange.md)


 

 