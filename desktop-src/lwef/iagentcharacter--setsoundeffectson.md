---
title: Иажентчарактер Сетсаундеффектсон
description: Иажентчарактер Сетсаундеффектсон
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710115"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="c86b8-103">Иажентчарактер:: Сетсаундеффектсон</span><span class="sxs-lookup"><span data-stu-id="c86b8-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="c86b8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c86b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="c86b8-105">Определяет, воспроизводятся ли звуковые эффекты символа.</span><span class="sxs-lookup"><span data-stu-id="c86b8-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="c86b8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c86b8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c86b8-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Системе*</span><span class="sxs-lookup"><span data-stu-id="c86b8-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="c86b8-108">Настройка звуковых эффектов.</span><span class="sxs-lookup"><span data-stu-id="c86b8-108">Sound effects setting.</span></span> <span data-ttu-id="c86b8-109">Если этот параметр имеет **значение true**, звуковые эффекты анимации воспроизводятся при воспроизведении анимации. Если задано **значение false**, звуковые эффекты не воспроизводятся.</span><span class="sxs-lookup"><span data-stu-id="c86b8-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="c86b8-110">Этот параметр определяет, будут ли воспроизводиться звуковые эффекты, скомпилированные как часть символа, при воспроизведении связанной анимации.</span><span class="sxs-lookup"><span data-stu-id="c86b8-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="c86b8-111">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="c86b8-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="c86b8-112">Этот параметр также подчиняется параметру глобальные звуковые эффекты пользователя в [**иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="c86b8-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c86b8-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="c86b8-113">See Also</span></span>

<span data-ttu-id="c86b8-114">[**Иажентчарактер:: жетсаундеффектсон**](iagentcharacter--getsoundeffectson.md), [ **иажентаудиуутпутпропертиес:: жетусингсаундеффектс**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="c86b8-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




