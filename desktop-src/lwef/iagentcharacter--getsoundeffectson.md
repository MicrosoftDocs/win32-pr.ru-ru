---
title: Иажентчарактер Жетсаундеффектсон
description: Иажентчарактер Жетсаундеффектсон
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691389"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="aeb42-103">Иажентчарактер:: Жетсаундеффектсон</span><span class="sxs-lookup"><span data-stu-id="aeb42-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="aeb42-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aeb42-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="aeb42-105">Получает значение, указывающее, включен ли параметр звуковых эффектов для символа.</span><span class="sxs-lookup"><span data-stu-id="aeb42-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="aeb42-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aeb42-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="aeb42-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*пбон*</span><span class="sxs-lookup"><span data-stu-id="aeb42-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="aeb42-108">Адрес переменной, принимающей **значение true** , если включен параметр звуковых эффектов для символа, **значение false** , если значение отключено.</span><span class="sxs-lookup"><span data-stu-id="aeb42-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="aeb42-109">Параметр звуковых эффектов для символа определяет, будут ли воспроизводиться звуковые эффекты, скомпилированные как часть символа, при воспроизведении связанной анимации.</span><span class="sxs-lookup"><span data-stu-id="aeb42-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="aeb42-110">Параметр подчиняется параметру глобальные звуковые эффекты пользователя в [**иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="aeb42-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aeb42-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="aeb42-111">See Also</span></span>

<span data-ttu-id="aeb42-112">[**Иажентчарактер:: сетсаундеффектсон**](iagentcharacter--setsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="aeb42-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




