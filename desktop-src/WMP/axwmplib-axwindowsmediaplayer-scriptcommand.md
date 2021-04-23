---
title: Событие команду скрипта объекта Аксвиндовсмедиаплайер
description: Событие команду скрипта возникает при получении синхронизированной команды или URL-адреса. | Событие команду скрипта объекта Аксвиндовсмедиаплайер
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Событие команду скрипта в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695042"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7e2c3-105">Событие команду скрипта объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="7e2c3-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7e2c3-106">Событие команду скрипта возникает при получении синхронизированной команды или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="7e2c3-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="7e2c3-107">Event Data</span></span>

<span data-ttu-id="7e2c3-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ скрипткоммандевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="7e2c3-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ скрипткоммандевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="7e2c3-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="7e2c3-110">Property</span></span> | <span data-ttu-id="7e2c3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7e2c3-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="7e2c3-112">сктипе</span><span class="sxs-lookup"><span data-stu-id="7e2c3-112">scType</span></span>   | <span data-ttu-id="7e2c3-113">System. СтрингспеЦифиес тип команды сценария.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="7e2c3-114">param</span><span class="sxs-lookup"><span data-stu-id="7e2c3-114">param</span></span>    | <span data-ttu-id="7e2c3-115">System. СтрингспеЦифиес. команда сценария.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="7e2c3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e2c3-116">Remarks</span></span>

<span data-ttu-id="7e2c3-117">Команды можно внедрять из звуков и изображений в файл или поток Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="7e2c3-118">Команды представляют собой пару строк в Юникоде, связанных с назначенным временем в потоке.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="7e2c3-119">Когда поток достигнет времени, связанного с командой, элемент управления проигрывателя Windows Media отправляет событие **команду скрипта** с двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="7e2c3-120">Один параметр указывает тип отправляемой команды, а другой параметр задает команду.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="7e2c3-121">Тип параметра используется для определения способа обработки параметра команды.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="7e2c3-122">Любой тип команды может быть внедрен в файл или поток для обработки событием **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7e2c3-123">В следующей таблице перечислены типы команд сценариев, которые автоматически обрабатываются проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="7e2c3-124">Тип</span><span class="sxs-lookup"><span data-stu-id="7e2c3-124">Type</span></span>                   | <span data-ttu-id="7e2c3-125">Описание</span><span class="sxs-lookup"><span data-stu-id="7e2c3-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2c3-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="7e2c3-126">CAPTION</span></span>                | <span data-ttu-id="7e2c3-127">Элемент управления отображает связанный текст в элементе HTML, указанном параметром Ивмпклоседкаптион. **каптионингид**.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="7e2c3-128">ЖУРНАЛЕ</span><span class="sxs-lookup"><span data-stu-id="7e2c3-128">EVENT</span></span>                  | <span data-ttu-id="7e2c3-129">Элемент управления выполняет инструкции, определенные для указанного события.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="7e2c3-130">ФАЙЛОВ</span><span class="sxs-lookup"><span data-stu-id="7e2c3-130">FILENAME</span></span>               | <span data-ttu-id="7e2c3-131">Элемент управления сбрасывает свойство **URL-адреса** , пытается открыть указанный файл и немедленно начинает воспроизведение нового потока.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="7e2c3-132">опеневент</span><span class="sxs-lookup"><span data-stu-id="7e2c3-132">OPENEVENT</span></span>              | <span data-ttu-id="7e2c3-133">Помещает связанную команду типа события в буфер для своевременного выполнения скрипта события.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="7e2c3-134">синчронизедлириклирик</span><span class="sxs-lookup"><span data-stu-id="7e2c3-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="7e2c3-135">Параметр *param* содержит синхронизированный текст лирик.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="7e2c3-136">Проигрыватель Windows Media отображает текст лирик в области скрытых субтитров в **воспроизводимой** функции.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="7e2c3-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="7e2c3-137">TEXT</span></span>                   | <span data-ttu-id="7e2c3-138">Элемент управления отображает связанный текст в элементе HTML, указанном параметром Ивмпклоседкаптион. **каптионингид**.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="7e2c3-139">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="7e2c3-139">URL</span></span>                    | <span data-ttu-id="7e2c3-140">Элемент управления автоматически открывает URL-адрес, указанный в браузере по умолчанию, если используется Ивмпсеттингс. Свойство **инвокеурлс** имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="7e2c3-141">Можно внедрить любой другой тип команды при условии, что код обрабатывает команду.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="7e2c3-142">Хотя неизвестные команды игнорируются элементом управления проигрывателем Windows Media, они по-прежнему передаются в событие **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="7e2c3-143">Событие команду скрипта не вызывается, если файл сканируется в режиме перемотки вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="7e2c3-144">Команды URL-адреса, получаемые элементом управления проигрывателем Windows Media, вызываются автоматически в веб-браузере по умолчанию, если Ивмпсеттингс. Свойство **инвокеурлс** имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="7e2c3-145">Можно использовать Ивмпсеттингс. Свойство **дефаултфраме** для указания целевого фрейма, в котором отображается веб-страница.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="7e2c3-146">URL-адрес, отправляемый проигрывателю Windows Media, обрабатывается относительно базового URL-адреса, указанного параметром Ивмпсеттингс. Свойство **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="7e2c3-147">Базовый URL-адрес объединяется с относительным URL-адресом, что приводит к полному URL-адресу, который передается событием **команду скрипта** в качестве параметра команды.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7e2c3-148">Элемент управления проигрывателя Windows Media всегда обрабатывает команды входящих URL-адресов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e2c3-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="7e2c3-149">Получена команда типа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="7e2c3-150">Ивмпсеттингс. **baseURL** используется для создания полного URL-адреса из относительного URL-адреса, указанного в команде скрипта.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="7e2c3-151">Вызывается **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="7e2c3-152">После **команду скрипта** возвращает ивмпсеттингс. **инвокеурлс** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="7e2c3-153">Если Ивмпсеттингс. **инвокеурлс** имеет значение true, а команда является командой URL-адреса, вызывается указанный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="7e2c3-154">Если Ивмпсеттингс. **инвокеурлс** имеет значение false или команда не является командой URL-адреса, команда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="7e2c3-155">При создании файла Windows Media можно указать кадр, в котором будет отображаться новый URL-адрес, объединяя два амперсанда и имя кадра в поле параметра.</span><span class="sxs-lookup"><span data-stu-id="7e2c3-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="7e2c3-156">В следующем примере показаны типичные параметры **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="7e2c3-157">Он указывает, что URL-адрес *MyPage* должен быть запущен в кадре *мифраме* .</span><span class="sxs-lookup"><span data-stu-id="7e2c3-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="7e2c3-158">Событие команду скрипта не вызывается, если файл сканируется (перемотка или перемотка вперед).</span><span class="sxs-lookup"><span data-stu-id="7e2c3-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2c3-159">Требования</span><span class="sxs-lookup"><span data-stu-id="7e2c3-159">Requirements</span></span>



| <span data-ttu-id="7e2c3-160">Требование</span><span class="sxs-lookup"><span data-stu-id="7e2c3-160">Requirement</span></span> | <span data-ttu-id="7e2c3-161">Значение</span><span class="sxs-lookup"><span data-stu-id="7e2c3-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2c3-162">Версия</span><span class="sxs-lookup"><span data-stu-id="7e2c3-162">Version</span></span><br/>   | <span data-ttu-id="7e2c3-163">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7e2c3-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7e2c3-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e2c3-164">Namespace</span></span><br/> | <span data-ttu-id="7e2c3-165">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7e2c3-166">Сборка</span><span class="sxs-lookup"><span data-stu-id="7e2c3-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e2c3-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e2c3-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e2c3-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e2c3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e2c3-169">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e2c3-170">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e2c3-171">**Ивмпклоседкаптион. Каптионингид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e2c3-172">**Ивмпсеттингс. baseURL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e2c3-173">**Ивмпсеттингс. Дефаултфраме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e2c3-174">**Ивмпсеттингс. Инвокеурлс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e2c3-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





