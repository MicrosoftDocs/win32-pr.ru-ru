---
description: Приложение использует методы этого интерфейса для реализации набора анимации по ключевым кадрам.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Интерфейс ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694287"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="53a62-103">Интерфейс ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="53a62-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="53a62-104">Приложение использует методы этого интерфейса для реализации набора анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="53a62-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="53a62-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="53a62-105">Members</span></span>

<span data-ttu-id="53a62-106">Интерфейс **ID3DXKeyframedAnimationSet** наследует от [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="53a62-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="53a62-107">**ID3DXKeyframedAnimationSet** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53a62-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="53a62-108">Методы</span><span class="sxs-lookup"><span data-stu-id="53a62-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="53a62-109">Методы</span><span class="sxs-lookup"><span data-stu-id="53a62-109">Methods</span></span>

<span data-ttu-id="53a62-110">Интерфейс **ID3DXKeyframedAnimationSet** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="53a62-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="53a62-111">Метод</span><span class="sxs-lookup"><span data-stu-id="53a62-111">Method</span></span>                                                                                   | <span data-ttu-id="53a62-112">Описание</span><span class="sxs-lookup"><span data-stu-id="53a62-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a62-113">**Сжатие**</span><span class="sxs-lookup"><span data-stu-id="53a62-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="53a62-114">Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="53a62-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="53a62-115">**жеткаллбакккэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="53a62-116">Возвращает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="53a62-117">**жеткаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="53a62-118">Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="53a62-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="53a62-119">**жетнумкаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="53a62-120">Возвращает число ключей обратного вызова в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="53a62-121">**жетнумротатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="53a62-122">Возвращает число ключей вращения в указанной анимации по опорным кадрам.</span><span class="sxs-lookup"><span data-stu-id="53a62-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="53a62-123">**жетнумскалекэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="53a62-124">Возвращает количество ключей масштабирования в указанной анимации по опорным кадрам.</span><span class="sxs-lookup"><span data-stu-id="53a62-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="53a62-125">**жетнумтранслатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="53a62-126">Возвращает число ключей перевода в указанной анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="53a62-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="53a62-127">**жетплайбакктипе**</span><span class="sxs-lookup"><span data-stu-id="53a62-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="53a62-128">Возвращает тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="53a62-129">**жетротатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="53a62-130">Получение сведений о повороте для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="53a62-131">**жетротатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="53a62-132">Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="53a62-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="53a62-133">**жетскалекэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="53a62-134">Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="53a62-135">**жетскалекэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="53a62-136">Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="53a62-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="53a62-137">**жетсаурцетикксперсеконд**</span><span class="sxs-lookup"><span data-stu-id="53a62-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="53a62-138">Возвращает число тактов кадра анимации, произошедших в секунду.</span><span class="sxs-lookup"><span data-stu-id="53a62-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="53a62-139">**жеттранслатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="53a62-140">Получение сведений о переводе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="53a62-141">**жеттранслатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="53a62-142">Заполняет массив данными ключа, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="53a62-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="53a62-143">**регистераниматионсрткэйс**</span><span class="sxs-lookup"><span data-stu-id="53a62-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="53a62-144">Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="53a62-145">**сеткаллбакккэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="53a62-146">Задает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="53a62-147">**сетротатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="53a62-148">Установка сведений о повороте для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="53a62-149">**сетскалекэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="53a62-150">Установка сведений о масштабе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="53a62-151">**сеттранслатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="53a62-152">Задание сведений о переводе для определенного ключевого кадра в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="53a62-153">**унрегистераниматион**</span><span class="sxs-lookup"><span data-stu-id="53a62-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="53a62-154">Удалите данные анимации из набора анимации.</span><span class="sxs-lookup"><span data-stu-id="53a62-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="53a62-155">**унрегистерротатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="53a62-156">Удаляет данные вращения в указанном опорном кадре.</span><span class="sxs-lookup"><span data-stu-id="53a62-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="53a62-157">**унрегистерскалекэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="53a62-158">Удаляет данные шкалы в указанном опорном кадре.</span><span class="sxs-lookup"><span data-stu-id="53a62-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="53a62-159">**унрегистертранслатионкэй**</span><span class="sxs-lookup"><span data-stu-id="53a62-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="53a62-160">Удаляет данные перевода в указанном опорном кадре.</span><span class="sxs-lookup"><span data-stu-id="53a62-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="53a62-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53a62-161">Remarks</span></span>

<span data-ttu-id="53a62-162">Создание набора анимации по ключевым кадрам с помощью [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="53a62-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="53a62-163">Тип LPD3DXKEYFRAMEDANIMATIONSET определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="53a62-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="53a62-164">Требования</span><span class="sxs-lookup"><span data-stu-id="53a62-164">Requirements</span></span>



| <span data-ttu-id="53a62-165">Требование</span><span class="sxs-lookup"><span data-stu-id="53a62-165">Requirement</span></span> | <span data-ttu-id="53a62-166">Значение</span><span class="sxs-lookup"><span data-stu-id="53a62-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53a62-167">Header</span><span class="sxs-lookup"><span data-stu-id="53a62-167">Header</span></span><br/>  | <dl> <span data-ttu-id="53a62-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a62-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="53a62-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53a62-169">Library</span></span><br/> | <dl> <span data-ttu-id="53a62-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53a62-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53a62-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53a62-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a62-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="53a62-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="53a62-173">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="53a62-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




