---
description: Метод Активатебуттон активирует выбранную кнопку меню.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Метод Активатебуттон
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682289"
---
# <a name="activatebutton-method"></a><span data-ttu-id="14b06-103">Метод Активатебуттон</span><span class="sxs-lookup"><span data-stu-id="14b06-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="14b06-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="14b06-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="14b06-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="14b06-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="14b06-106">Метод Активатебуттон активирует выбранную кнопку меню.</span><span class="sxs-lookup"><span data-stu-id="14b06-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="14b06-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b06-107">Return Value</span></span>

<span data-ttu-id="14b06-108">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="14b06-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b06-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14b06-109">Remarks</span></span>

<span data-ttu-id="14b06-110">Используйте этот метод при реализации пользовательской обработки мыши после установки для [**дисаблеаутомаусепроцессинг**](disableautomouseprocessing-property.md) значения **true**.</span><span class="sxs-lookup"><span data-stu-id="14b06-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="14b06-111">Этот метод используется для активации кнопки, выбранной с помощью метода [**селектлефтбуттон**](selectleftbutton-method.md), [**селектловербуттон**](selectlowerbutton-method.md), [**селектуппербуттон**](selectupperbutton-method.md)или [**селектригхтбуттон**](selectrightbutton-method.md) .</span><span class="sxs-lookup"><span data-stu-id="14b06-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



