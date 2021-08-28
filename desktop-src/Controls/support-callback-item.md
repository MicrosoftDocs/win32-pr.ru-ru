---
title: Поддержка элементов обратного вызова
description: В этом разделе показано, как обеспечить поддержку элементов обратного вызова.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df078b8be8cd02f56592a74de4242b515974a740df01d3cd4bd36074d5f8e022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968224"
---
# <a name="how-to-support-callback-items"></a>Поддержка элементов обратного вызова

В этом разделе показано, как обеспечить поддержку элементов обратного вызова.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Если приложение будет использовать элементы обратного вызова в элементе управления ComboBoxEx, необходимо подготовиться к обработке кода уведомления [ \_ жетдиспинфо кбен](cben-getdispinfo.md) . Элемент управления ComboBoxEx отправляет это уведомление каждый раз, когда ему нужен владелец для предоставления конкретных сведений об элементе. Дополнительные сведения об элементах обратного вызова см. в разделе [элементы обратного](comboboxex-controls.md)вызова.

Следующая определяемая приложением функция обрабатывает [кбен \_ жетдиспинфо](cben-getdispinfo.md) , предоставляя атрибуты для данного элемента. Обратите внимание, что он устанавливает для элемента **маски** входящей [**КОМБОБОКСЕКСИТЕМ**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) структуры значение кбеиф \_ di \_ сетитем. Если задать **маску** для этого значения, элемент управления будет хранить сведения об элементе, чтобы не запрашивать эти сведения еще раз.

## <a name="complete-example"></a>Полный пример


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об элементах управления ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Справочник по элементу управления ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Использование элементов управления ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 