---
title: Событие Player. команду скрипта
description: Событие команду скрипта возникает при получении синхронизированной команды или URL-адреса. | Событие Player. команду скрипта
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Проигрыватель Windows Media Event команду скрипта
- Проигрыватель Windows Media Event команду скрипта, класс Player
- Класс проигрывателя Windows Media Player, событие команду скрипта
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708626"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="02d39-107">Событие Player. команду скрипта</span><span class="sxs-lookup"><span data-stu-id="02d39-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="02d39-108">Событие **команду скрипта** возникает при получении синхронизированной команды или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="02d39-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d39-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02d39-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="02d39-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="02d39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d39-111">*сктипе*</span><span class="sxs-lookup"><span data-stu-id="02d39-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="02d39-112">Строка, указывающая тип команды скрипта.</span><span class="sxs-lookup"><span data-stu-id="02d39-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="02d39-113">*Байт*</span><span class="sxs-lookup"><span data-stu-id="02d39-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="02d39-114">**Строка** , указывающая команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="02d39-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d39-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02d39-115">Return value</span></span>

<span data-ttu-id="02d39-116">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="02d39-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02d39-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02d39-117">Remarks</span></span>

<span data-ttu-id="02d39-118">Команды можно внедрять из звуков и изображений в файл или поток Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02d39-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="02d39-119">Команды представляют собой пару строк в Юникоде, связанных с назначенным временем в потоке.</span><span class="sxs-lookup"><span data-stu-id="02d39-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="02d39-120">Когда поток достигнет времени, связанного с командой, элемент управления проигрывателя Windows Media отправляет событие **команду скрипта** с двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="02d39-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="02d39-121">Один параметр указывает тип отправляемой команды, а другой параметр задает команду.</span><span class="sxs-lookup"><span data-stu-id="02d39-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="02d39-122">Тип параметра используется для определения способа обработки параметра команды.</span><span class="sxs-lookup"><span data-stu-id="02d39-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="02d39-123">Любой тип команды может быть внедрен в файл или поток для обработки событием **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="02d39-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="02d39-124">В следующей таблице перечислены типы команд сценариев, которые автоматически обрабатываются проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02d39-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="02d39-125">Тип</span><span class="sxs-lookup"><span data-stu-id="02d39-125">Type</span></span>                   | <span data-ttu-id="02d39-126">Описание</span><span class="sxs-lookup"><span data-stu-id="02d39-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d39-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="02d39-127">CAPTION</span></span>                | <span data-ttu-id="02d39-128">Элемент управления отображает связанный текст в DIV, заданном параметром *клоседкаптион*. **каптионингид**.</span><span class="sxs-lookup"><span data-stu-id="02d39-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="02d39-129">ЖУРНАЛЕ</span><span class="sxs-lookup"><span data-stu-id="02d39-129">EVENT</span></span>                  | <span data-ttu-id="02d39-130">Указывает элементу управления на выполнение инструкций, определенных для указанного события.</span><span class="sxs-lookup"><span data-stu-id="02d39-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="02d39-131">ФАЙЛОВ</span><span class="sxs-lookup"><span data-stu-id="02d39-131">FILENAME</span></span>               | <span data-ttu-id="02d39-132">Элемент управления сбрасывает свойство **URL-адреса** , пытается открыть указанный файл и немедленно начинает воспроизведение нового потока.</span><span class="sxs-lookup"><span data-stu-id="02d39-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="02d39-133">опеневент</span><span class="sxs-lookup"><span data-stu-id="02d39-133">OPENEVENT</span></span>              | <span data-ttu-id="02d39-134">Помещает связанную команду типа события в буфер для своевременного выполнения скрипта события.</span><span class="sxs-lookup"><span data-stu-id="02d39-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="02d39-135">синчронизедлириклирик</span><span class="sxs-lookup"><span data-stu-id="02d39-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="02d39-136">Параметр *param* содержит синхронизированный текст лирик.</span><span class="sxs-lookup"><span data-stu-id="02d39-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="02d39-137">Проигрыватель Windows Media отображает текст лирик в области скрытых субтитров в **воспроизводимой** функции.</span><span class="sxs-lookup"><span data-stu-id="02d39-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="02d39-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="02d39-138">TEXT</span></span>                   | <span data-ttu-id="02d39-139">Элемент управления отображает связанный текст в DIV, заданном параметром *клоседкаптион*. **каптионингид**.</span><span class="sxs-lookup"><span data-stu-id="02d39-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="02d39-140">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="02d39-140">URL</span></span>                    | <span data-ttu-id="02d39-141">Этот элемент управления автоматически открывает URL-адрес, указанный с помощью браузера по умолчанию, если *Параметры*. Свойство **инвокеурлс** имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="02d39-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="02d39-142">Можно внедрить любой другой тип команды при условии, что вы предоставляете для выполнения команды взаимный код.</span><span class="sxs-lookup"><span data-stu-id="02d39-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="02d39-143">Хотя неизвестные команды игнорируются элементом управления проигрывателем Windows Media, они по-прежнему передаются в событие **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="02d39-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="02d39-144">Команды URL-адреса, получаемые элементом управления проигрывателем Windows Media, вызываются автоматически в веб-браузере по умолчанию, если *Параметры*. Свойство **инвокеурлс** имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="02d39-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="02d39-145">Можно использовать *Параметры*. Свойство **дефаултфраме** для указания целевого фрейма, в котором отображается веб-страница.</span><span class="sxs-lookup"><span data-stu-id="02d39-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="02d39-146">URL-адрес, отправляемый проигрывателю Windows Media, обрабатывается относительно базового URL-адреса, указанного в *параметрах*. Свойство **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="02d39-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="02d39-147">Базовый URL-адрес объединяется с относительно указанным URL-адресом, что приводит к полному URL-адресу, который передается в качестве параметра команды событием **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="02d39-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="02d39-148">Элемент управления проигрывателя Windows Media всегда обрабатывает входящие команды типа URL-адреса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="02d39-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="02d39-149">Получена команда типа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="02d39-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="02d39-150">*Параметры*. **baseURL** используется для создания полного URL-адреса из относительного URL-адреса, указанного в команде скрипта.</span><span class="sxs-lookup"><span data-stu-id="02d39-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="02d39-151">Вызывается *команду скрипта* .</span><span class="sxs-lookup"><span data-stu-id="02d39-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="02d39-152">После *команду скрипта* возвращает *Параметры*. **инвокеурлс** .</span><span class="sxs-lookup"><span data-stu-id="02d39-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="02d39-153">Если *Параметры*. **инвокеурлс** имеет значение true, а команда является URL-типом, вызывается указанный URL.</span><span class="sxs-lookup"><span data-stu-id="02d39-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="02d39-154">Если *Параметры*. **инвокеурлс** имеет значение false или если команда не является типом URL-адреса, команда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="02d39-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="02d39-155">При создании файла Windows Media можно указать кадр, в котором будет отображаться новый URL-адрес, объединяя два амперсанда и имя кадра в поле параметра.</span><span class="sxs-lookup"><span data-stu-id="02d39-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="02d39-156">В приведенном ниже примере показаны стандартные параметры *команду скрипта* .</span><span class="sxs-lookup"><span data-stu-id="02d39-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="02d39-157">Он указывает, что URL-адрес *MyPage* должен быть запущен в кадре *мифраме* .</span><span class="sxs-lookup"><span data-stu-id="02d39-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="02d39-158">Событие команду скрипта не вызывается, если файл сканируется (перемотка вперед или быстро).</span><span class="sxs-lookup"><span data-stu-id="02d39-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="02d39-159">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="02d39-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="02d39-160">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="02d39-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d39-161">Требования</span><span class="sxs-lookup"><span data-stu-id="02d39-161">Requirements</span></span>



| <span data-ttu-id="02d39-162">Требование</span><span class="sxs-lookup"><span data-stu-id="02d39-162">Requirement</span></span> | <span data-ttu-id="02d39-163">Значение</span><span class="sxs-lookup"><span data-stu-id="02d39-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02d39-164">Версия</span><span class="sxs-lookup"><span data-stu-id="02d39-164">Version</span></span><br/> | <span data-ttu-id="02d39-165">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="02d39-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="02d39-166">DLL</span><span class="sxs-lookup"><span data-stu-id="02d39-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="02d39-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d39-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d39-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02d39-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d39-169">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="02d39-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="02d39-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="02d39-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="02d39-171">**Settings. baseURL**</span><span class="sxs-lookup"><span data-stu-id="02d39-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="02d39-172">**Settings. Дефаултфраме**</span><span class="sxs-lookup"><span data-stu-id="02d39-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="02d39-173">**Settings. Инвокеурлс**</span><span class="sxs-lookup"><span data-stu-id="02d39-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





