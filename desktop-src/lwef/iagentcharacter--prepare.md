---
title: Подготовка Иажентчарактер
description: Подготовка Иажентчарактер
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069970"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="dac89-103">Иажентчарактер::P готовка</span><span class="sxs-lookup"><span data-stu-id="dac89-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="dac89-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dac89-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="dac89-105">Извлекает данные анимации для символа.</span><span class="sxs-lookup"><span data-stu-id="dac89-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="dac89-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dac89-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="dac89-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="dac89-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="dac89-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*двтипе*</span><span class="sxs-lookup"><span data-stu-id="dac89-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="dac89-109">Значение, указывающее тип данных анимации для загрузки, который должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="dac89-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="dac89-110">Значение</span><span class="sxs-lookup"><span data-stu-id="dac89-110">Value</span></span>                                                           | <span data-ttu-id="dac89-111">Описание</span><span class="sxs-lookup"><span data-stu-id="dac89-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="dac89-112">**неподписанная короткая анимация без знака в константе** **\_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="dac89-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="dac89-113">Данные анимации символа.</span><span class="sxs-lookup"><span data-stu-id="dac89-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="dac89-114">**постоянное неподписанное короткое** **состояние подготавливается \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="dac89-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="dac89-115">Данные о состоянии символа.</span><span class="sxs-lookup"><span data-stu-id="dac89-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="dac89-116">**константа неподписанного короткого файла подписывания const** **\_ = 2**</span><span class="sxs-lookup"><span data-stu-id="dac89-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="dac89-117">Звуковой файл символа (. WAV или. ЛВВ) для речевого вывода.</span><span class="sxs-lookup"><span data-stu-id="dac89-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="dac89-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*</span><span class="sxs-lookup"><span data-stu-id="dac89-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="dac89-119">Имя анимации или состояния.</span><span class="sxs-lookup"><span data-stu-id="dac89-119">The name of the animation or state.</span></span>

<span data-ttu-id="dac89-120">Имя анимации основано на том, что определено для символа при его сохранении с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="dac89-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="dac89-121">Для состояний может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="dac89-121">For states, the value can be one of the following:</span></span>



|                      |                                                 |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="dac89-122">**"Жестуринг"**</span><span class="sxs-lookup"><span data-stu-id="dac89-122">**"Gesturing"**</span></span>      | <span data-ttu-id="dac89-123">Для получения всех анимаций состояния **жестуринг** .</span><span class="sxs-lookup"><span data-stu-id="dac89-123">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="dac89-124">**"Жестурингдовн"**</span><span class="sxs-lookup"><span data-stu-id="dac89-124">**"GesturingDown"**</span></span>  | <span data-ttu-id="dac89-125">Для получения анимации **жестурингдовн** .</span><span class="sxs-lookup"><span data-stu-id="dac89-125">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="dac89-126">**"Жестуринглефт"**</span><span class="sxs-lookup"><span data-stu-id="dac89-126">**"GesturingLeft"**</span></span>  | <span data-ttu-id="dac89-127">Для получения анимации **жестуринглефт** .</span><span class="sxs-lookup"><span data-stu-id="dac89-127">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="dac89-128">**"Жестурингригхт"**</span><span class="sxs-lookup"><span data-stu-id="dac89-128">**"GesturingRight"**</span></span> | <span data-ttu-id="dac89-129">Для получения анимации **жестурингригхт** .</span><span class="sxs-lookup"><span data-stu-id="dac89-129">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="dac89-130">**"Жестурингуп"**</span><span class="sxs-lookup"><span data-stu-id="dac89-130">**"GesturingUp"**</span></span>    | <span data-ttu-id="dac89-131">Для получения анимации **жестурингуп** .</span><span class="sxs-lookup"><span data-stu-id="dac89-131">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="dac89-132">**Отображение**</span><span class="sxs-lookup"><span data-stu-id="dac89-132">**"Hiding"**</span></span>         | <span data-ttu-id="dac89-133">Для получения анимации **скрытого** состояния.</span><span class="sxs-lookup"><span data-stu-id="dac89-133">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="dac89-134">**Движ**</span><span class="sxs-lookup"><span data-stu-id="dac89-134">**"Hearing"**</span></span>        | <span data-ttu-id="dac89-135">Для получения анимации состояния **слуха** .</span><span class="sxs-lookup"><span data-stu-id="dac89-135">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="dac89-136">**Состояние простоя**</span><span class="sxs-lookup"><span data-stu-id="dac89-136">**"Idling"**</span></span>         | <span data-ttu-id="dac89-137">Для получения всех анимаций состояния **состояние простоя** .</span><span class="sxs-lookup"><span data-stu-id="dac89-137">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="dac89-138">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="dac89-138">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="dac89-139">Для получения всех анимаций **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="dac89-139">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="dac89-140">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="dac89-140">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="dac89-141">Для получения всех анимаций **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="dac89-141">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="dac89-142">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="dac89-142">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="dac89-143">Для получения всех анимаций **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="dac89-143">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="dac89-144">**Прослушивающий**</span><span class="sxs-lookup"><span data-stu-id="dac89-144">**"Listening"**</span></span>      | <span data-ttu-id="dac89-145">Для получения анимации состояния **прослушивания** .</span><span class="sxs-lookup"><span data-stu-id="dac89-145">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="dac89-146">**Изменения**</span><span class="sxs-lookup"><span data-stu-id="dac89-146">**"Moving"**</span></span>         | <span data-ttu-id="dac89-147">Для получения всех анимаций о состоянии **перемещения** .</span><span class="sxs-lookup"><span data-stu-id="dac89-147">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="dac89-148">**"Мовингдовн"**</span><span class="sxs-lookup"><span data-stu-id="dac89-148">**"MovingDown"**</span></span>     | <span data-ttu-id="dac89-149">Для получения всех **движущихся** анимаций.</span><span class="sxs-lookup"><span data-stu-id="dac89-149">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="dac89-150">**"Мовинглефт"**</span><span class="sxs-lookup"><span data-stu-id="dac89-150">**"MovingLeft"**</span></span>     | <span data-ttu-id="dac89-151">Для получения всех анимаций **мовинглефт** .</span><span class="sxs-lookup"><span data-stu-id="dac89-151">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="dac89-152">**"Мовингригхт"**</span><span class="sxs-lookup"><span data-stu-id="dac89-152">**"MovingRight"**</span></span>    | <span data-ttu-id="dac89-153">Для получения всех анимаций **мовингригхт** .</span><span class="sxs-lookup"><span data-stu-id="dac89-153">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="dac89-154">**"Мовингуп"**</span><span class="sxs-lookup"><span data-stu-id="dac89-154">**"MovingUp"**</span></span>       | <span data-ttu-id="dac89-155">Для получения всех анимаций **мовингуп** .</span><span class="sxs-lookup"><span data-stu-id="dac89-155">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="dac89-156">**Специаль**</span><span class="sxs-lookup"><span data-stu-id="dac89-156">**"Showing"**</span></span>        | <span data-ttu-id="dac89-157">Для получения анимации состояния **отображения** .</span><span class="sxs-lookup"><span data-stu-id="dac89-157">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="dac89-158">**Говоря**</span><span class="sxs-lookup"><span data-stu-id="dac89-158">**"Speaking"**</span></span>       | <span data-ttu-id="dac89-159">Для получения анимации состояния **речи** .</span><span class="sxs-lookup"><span data-stu-id="dac89-159">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="dac89-160">Предмет. Файлы WAV, задайте для *бсзнаме* URL-адрес или спецификацию файла для. Файл WAV.</span><span class="sxs-lookup"><span data-stu-id="dac89-160">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="dac89-161">Если спецификация не завершена, она интерпретируется как относительная для спецификации, используемой в методе [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="dac89-161">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="dac89-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*бкуеуе*</span><span class="sxs-lookup"><span data-stu-id="dac89-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="dac89-163">Логическое значение, указывающее, помещает ли сервер запрос на [**подготовку**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="dac89-163">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="dac89-164">**Значение true** ставит запрос в очередь и приводит к тому, что все запросы анимации, которые следуют за ним, ожидают загрузки данных анимации, которые он указывает.</span><span class="sxs-lookup"><span data-stu-id="dac89-164">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="dac89-165">**Значение false** — возвращает данные анимации асинхронно.</span><span class="sxs-lookup"><span data-stu-id="dac89-165">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="dac89-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="dac89-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="dac89-167">Адрес переменной, которая получает идентификатор запроса на [**подготовку**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="dac89-167">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="dac89-168">При загрузке символа с помощью протокола HTTP (. ACF File) необходимо использовать метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) для получения данных анимации, прежде чем можно будет воспроизвести анимацию.</span><span class="sxs-lookup"><span data-stu-id="dac89-168">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="dac89-169">Этот метод нельзя использовать, если вы загрузили символ с помощью протокола UNC (. Файл ACS).</span><span class="sxs-lookup"><span data-stu-id="dac89-169">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="dac89-170">Вы также не можете получить данные HTTP для символа с помощью инструкции **Prepare** , если вы загрузили этот символ с помощью протокола UNC (. Файл символов ACS).</span><span class="sxs-lookup"><span data-stu-id="dac89-170">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="dac89-171">Анимация или звуковые данные, полученные с помощью метода [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , хранятся в кэше браузера.</span><span class="sxs-lookup"><span data-stu-id="dac89-171">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="dac89-172">Последующие вызовы проверяют кэш и, если данные анимации уже есть, элемент управления загружает данные непосредственно из кэша.</span><span class="sxs-lookup"><span data-stu-id="dac89-172">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="dac89-173">После загрузки анимации или звуковые данные можно воспроизвести с помощью методов [**Play**](/windows/desktop/lwef/iagentcharacter--play) или [**говорите**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="dac89-173">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="dac89-174">Можно указать несколько анимаций и состояний, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="dac89-174">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="dac89-175">Однако нельзя смешивать типы в одной и той же инструкции [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="dac89-175">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

