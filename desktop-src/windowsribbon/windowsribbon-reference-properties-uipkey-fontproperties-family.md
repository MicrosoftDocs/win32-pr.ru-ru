---
title: UI_PKEY_FontProperties_Family
description: Идентифицирует свойство UI \_ PKEY \_ фонтпропертиес \_ Family.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710293"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="b22c4-103">\_Семейство UI PKEY \_ фонтпропертиес \_</span><span class="sxs-lookup"><span data-stu-id="b22c4-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="b22c4-104">Идентифицирует свойство UI \_ PKEY \_ фонтпропертиес \_ Family.</span><span class="sxs-lookup"><span data-stu-id="b22c4-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="b22c4-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b22c4-105">Remarks</span></span>

<span data-ttu-id="b22c4-106">\_Семейство UI PKEY \_ фонтпропертиес \_ используется приложением для запроса значения раскрывающейся коллекции **семейства шрифтов** .</span><span class="sxs-lookup"><span data-stu-id="b22c4-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="b22c4-107">Значение \_ семейства ФОНТПРОПЕРТИЕС UI PKEY \_ \_ соответствует имени [семейства шрифтов Windows GDI](../gdi/font-families.md) , полученному с помощью [функции EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) или [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span><span class="sxs-lookup"><span data-stu-id="b22c4-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="b22c4-108">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="b22c4-108">The default value is an empty string.</span></span>

<span data-ttu-id="b22c4-109">Если в качестве значения для семейства фонтпропертиес UI PKEY указана пустая строка \_ \_ \_ , выделение шрифта снимается.</span><span class="sxs-lookup"><span data-stu-id="b22c4-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b22c4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b22c4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b22c4-111">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="b22c4-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="b22c4-112">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="b22c4-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 