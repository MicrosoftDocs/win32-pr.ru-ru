---
title: Подготовка Иажентчарактер
description: Подготовка Иажентчарактер
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119879"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="4f0ee-103">Иажентчарактер::P готовка</span><span class="sxs-lookup"><span data-stu-id="4f0ee-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="4f0ee-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f0ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="4f0ee-105">Извлекает данные анимации для символа.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="4f0ee-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="4f0ee-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="4f0ee-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*двтипе*</span><span class="sxs-lookup"><span data-stu-id="4f0ee-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="4f0ee-109">Значение, указывающее тип данных анимации для загрузки, который должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="4f0ee-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="4f0ee-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4f0ee-110">Value</span></span>                                                           | <span data-ttu-id="4f0ee-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4f0ee-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f0ee-112">**неподписанная короткая анимация без знака в константе** **\_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="4f0ee-113">Данные анимации символа.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="4f0ee-114">**постоянное неподписанное короткое** **состояние подготавливается \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="4f0ee-115">Данные о состоянии символа.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="4f0ee-116">**константа неподписанного короткого файла подписывания const** **\_ = 2**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="4f0ee-117">Звуковой файл символа (. WAV или. ЛВВ) для речевого вывода.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4f0ee-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*</span><span class="sxs-lookup"><span data-stu-id="4f0ee-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="4f0ee-119">Имя анимации или состояния.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-119">The name of the animation or state.</span></span>

<span data-ttu-id="4f0ee-120">Имя анимации основано на том, что определено для символа при его сохранении с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="4f0ee-121">Для состояний может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4f0ee-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="4f0ee-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4f0ee-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="4f0ee-123">**"Жестуринг"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-123">**"Gesturing"**</span></span>      | <span data-ttu-id="4f0ee-124">Для получения всех анимаций состояния **жестуринг** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="4f0ee-125">**"Жестурингдовн"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="4f0ee-126">Для получения анимации **жестурингдовн** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="4f0ee-127">**"Жестуринглефт"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="4f0ee-128">Для получения анимации **жестуринглефт** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="4f0ee-129">**"Жестурингригхт"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-129">**"GesturingRight"**</span></span> | <span data-ttu-id="4f0ee-130">Для получения анимации **жестурингригхт** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="4f0ee-131">**"Жестурингуп"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="4f0ee-132">Для получения анимации **жестурингуп** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="4f0ee-133">**Отображение**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-133">**"Hiding"**</span></span>         | <span data-ttu-id="4f0ee-134">Для получения анимации **скрытого** состояния.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="4f0ee-135">**Движ**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-135">**"Hearing"**</span></span>        | <span data-ttu-id="4f0ee-136">Для получения анимации состояния **слуха** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="4f0ee-137">**Состояние простоя**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-137">**"Idling"**</span></span>         | <span data-ttu-id="4f0ee-138">Для получения всех анимаций состояния **состояние простоя** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="4f0ee-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="4f0ee-140">Для получения всех анимаций **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="4f0ee-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="4f0ee-142">Для получения всех анимаций **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="4f0ee-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="4f0ee-144">Для получения всех анимаций **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="4f0ee-145">**Прослушивающий**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-145">**"Listening"**</span></span>      | <span data-ttu-id="4f0ee-146">Для получения анимации состояния **прослушивания** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="4f0ee-147">**Изменения**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-147">**"Moving"**</span></span>         | <span data-ttu-id="4f0ee-148">Для получения всех анимаций о состоянии **перемещения** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="4f0ee-149">**"Мовингдовн"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-149">**"MovingDown"**</span></span>     | <span data-ttu-id="4f0ee-150">Для получения всех **движущихся** анимаций.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="4f0ee-151">**"Мовинглефт"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="4f0ee-152">Для получения всех анимаций **мовинглефт** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="4f0ee-153">**"Мовингригхт"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-153">**"MovingRight"**</span></span>    | <span data-ttu-id="4f0ee-154">Для получения всех анимаций **мовингригхт** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="4f0ee-155">**"Мовингуп"**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-155">**"MovingUp"**</span></span>       | <span data-ttu-id="4f0ee-156">Для получения всех анимаций **мовингуп** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="4f0ee-157">**Специаль**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-157">**"Showing"**</span></span>        | <span data-ttu-id="4f0ee-158">Для получения анимации состояния **отображения** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="4f0ee-159">**Говоря**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-159">**"Speaking"**</span></span>       | <span data-ttu-id="4f0ee-160">Для получения анимации состояния **речи** .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="4f0ee-161">Предмет. Файлы WAV, задайте для *бсзнаме* URL-адрес или спецификацию файла для. Файл WAV.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="4f0ee-162">Если спецификация не завершена, она интерпретируется как относительная для спецификации, используемой в методе [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="4f0ee-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*бкуеуе*</span><span class="sxs-lookup"><span data-stu-id="4f0ee-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="4f0ee-164">Логическое значение, указывающее, помещает ли сервер запрос на [**подготовку**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="4f0ee-165">**Значение true** ставит запрос в очередь и приводит к тому, что все запросы анимации, которые следуют за ним, ожидают загрузки данных анимации, которые он указывает.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="4f0ee-166">**Значение false** — возвращает данные анимации асинхронно.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="4f0ee-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="4f0ee-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="4f0ee-168">Адрес переменной, которая получает идентификатор запроса на [**подготовку**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="4f0ee-169">При загрузке символа с помощью протокола HTTP (. ACF File) необходимо использовать метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) для получения данных анимации, прежде чем можно будет воспроизвести анимацию.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="4f0ee-170">Этот метод нельзя использовать, если вы загрузили символ с помощью протокола UNC (. Файл ACS).</span><span class="sxs-lookup"><span data-stu-id="4f0ee-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="4f0ee-171">Вы также не можете получить данные HTTP для символа с помощью инструкции **Prepare** , если вы загрузили этот символ с помощью протокола UNC (. Файл символов ACS).</span><span class="sxs-lookup"><span data-stu-id="4f0ee-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="4f0ee-172">Анимация или звуковые данные, полученные с помощью метода [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , хранятся в кэше браузера.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="4f0ee-173">Последующие вызовы проверяют кэш и, если данные анимации уже есть, элемент управления загружает данные непосредственно из кэша.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="4f0ee-174">После загрузки анимации или звуковые данные можно воспроизвести с помощью методов [**Play**](/windows/desktop/lwef/iagentcharacter--play) или [**говорите**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="4f0ee-175">Можно указать несколько анимаций и состояний, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="4f0ee-176">Однако нельзя смешивать типы в одной и той же инструкции [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="4f0ee-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

