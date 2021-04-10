---
title: Иажентчарактер показывать
description: Иажентчарактер показывать
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070007"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="94e82-103">Иажентчарактер:: показывать</span><span class="sxs-lookup"><span data-stu-id="94e82-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="94e82-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94e82-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="94e82-105">Отображает символ.</span><span class="sxs-lookup"><span data-stu-id="94e82-105">Displays a character.</span></span>

-   <span data-ttu-id="94e82-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="94e82-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="94e82-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="94e82-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="94e82-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*бфаст*</span><span class="sxs-lookup"><span data-stu-id="94e82-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="94e82-109">Отображение флага анимации состояния.</span><span class="sxs-lookup"><span data-stu-id="94e82-109">Showing state animation flag.</span></span> <span data-ttu-id="94e82-110">Если этот параметр имеет **значение true**, анимация **отображения** состояния воспроизводится после того, как символ виден. Если задано **значение false**, анимация не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="94e82-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="94e82-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="94e82-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="94e82-112">Адрес переменной, которая получает идентификатор запроса на [**Отображение**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="94e82-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="94e82-113">Избегайте установки значения **true** для параметра *бфаст* без предварительного воспроизведения анимации; в противном случае рамка символов может отображаться, но не иметь изображения для отображения.</span><span class="sxs-lookup"><span data-stu-id="94e82-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="94e82-114">В частности, обратите внимание, что при вызове функции [**MoveTo**](iagentcharacter--moveto.md) , если символ не отображается, анимация не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="94e82-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="94e82-115">Поэтому при вызове метода " **Показать** " с параметром *бфаст* , для которого задано значение **true**, изображение отображаться не будет.</span><span class="sxs-lookup"><span data-stu-id="94e82-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="94e82-116">Аналогично, если вызвать [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), а затем **Показать** , что для *бфаст* задано значение **true**, изображение не будет отображено.</span><span class="sxs-lookup"><span data-stu-id="94e82-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="94e82-117">При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность анимации **отображаемого** состояния перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="94e82-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="94e82-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="94e82-118">See Also</span></span>

[<span data-ttu-id="94e82-119">**Иажентчарактер:: Hide**</span><span class="sxs-lookup"><span data-stu-id="94e82-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 