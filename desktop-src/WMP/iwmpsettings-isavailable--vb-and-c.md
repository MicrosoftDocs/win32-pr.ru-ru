---
title: Ивмпсеттингс. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) возвращает значение, указывающее, можно ли выполнить указанное действие.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- Проигрыватель Windows Media Ивмпсеттингс. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694658"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="4100d-104">Ивмпсеттингс. доступ (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="4100d-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="4100d-105">Свойство **Available** (метод Get- **\_ Available** в C#) возвращает значение, указывающее, можно ли выполнить указанное действие.</span><span class="sxs-lookup"><span data-stu-id="4100d-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="4100d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4100d-106">Parameters</span></span>

<span data-ttu-id="4100d-107">*бстритем*</span><span class="sxs-lookup"><span data-stu-id="4100d-107">*bstrItem*</span></span>

<span data-ttu-id="4100d-108">**Строка System. String** , которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4100d-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="4100d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="4100d-109">Value</span></span>              | <span data-ttu-id="4100d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4100d-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4100d-111">автозапуск</span><span class="sxs-lookup"><span data-stu-id="4100d-111">AutoStart</span></span>          | <span data-ttu-id="4100d-112">Обнаруживает, можно ли задать свойство автозапуска, чтобы указать, что проигрыватель Windows Media автоматически запускает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="4100d-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="4100d-113">Balance</span><span class="sxs-lookup"><span data-stu-id="4100d-113">Balance</span></span>            | <span data-ttu-id="4100d-114">Обнаруживает, можно ли использовать свойство Balance для установки баланса стерео.</span><span class="sxs-lookup"><span data-stu-id="4100d-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="4100d-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="4100d-115">BaseURL</span></span>            | <span data-ttu-id="4100d-116">Обнаруживает, можно ли задать свойство baseURL для указания базового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="4100d-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="4100d-117">дефаултфраме</span><span class="sxs-lookup"><span data-stu-id="4100d-117">DefaultFrame</span></span>       | <span data-ttu-id="4100d-118">Обнаруживает, можно ли задать свойство Дефаултфраме, чтобы указать кадр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4100d-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="4100d-119">енаблиррордиалогс</span><span class="sxs-lookup"><span data-stu-id="4100d-119">EnableErrorDialogs</span></span> | <span data-ttu-id="4100d-120">Обнаруживает, можно ли установить свойство Енаблиррордиалогс для включения или отключения отображения диалоговых окон ошибок.</span><span class="sxs-lookup"><span data-stu-id="4100d-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="4100d-121">Режим</span><span class="sxs-lookup"><span data-stu-id="4100d-121">GetMode</span></span>            | <span data-ttu-id="4100d-122">Обнаруживает, можно ли использовать метод метода мода для получения текущего цикла или режима "в случайном порядке".</span><span class="sxs-lookup"><span data-stu-id="4100d-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="4100d-123">инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="4100d-123">InvokeURLs</span></span>         | <span data-ttu-id="4100d-124">Обнаруживает, можно ли задать свойство Инвокеурлс, чтобы указать, должны ли события URL запускаться в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="4100d-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="4100d-125">Mute</span><span class="sxs-lookup"><span data-stu-id="4100d-125">Mute</span></span>               | <span data-ttu-id="4100d-126">Обнаруживает, можно ли задать свойство «выкл.», чтобы указать, включены ли звуковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="4100d-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="4100d-127">плайкаунт</span><span class="sxs-lookup"><span data-stu-id="4100d-127">PlayCount</span></span>          | <span data-ttu-id="4100d-128">Обнаруживает, можно ли задать свойство Плайкаунт, чтобы указать число попыток воспроизведения элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4100d-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="4100d-129">Тариф</span><span class="sxs-lookup"><span data-stu-id="4100d-129">Rate</span></span>               | <span data-ttu-id="4100d-130">Обнаруживает, можно ли задать свойство Rate для управления скоростью воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4100d-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="4100d-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="4100d-131">SetMode</span></span>            | <span data-ttu-id="4100d-132">Обнаруживает, можно ли использовать метод setMode для указания текущего цикла или режима "в случайном порядке".</span><span class="sxs-lookup"><span data-stu-id="4100d-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="4100d-133">Том</span><span class="sxs-lookup"><span data-stu-id="4100d-133">Volume</span></span>             | <span data-ttu-id="4100d-134">Обнаруживает, можно ли задать для свойства Volume громкость звука.</span><span class="sxs-lookup"><span data-stu-id="4100d-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="4100d-135">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4100d-135">Property Value</span></span>

<span data-ttu-id="4100d-136">Значение **System. Boolean** , указывающее, можно ли выполнить указанное действие.</span><span class="sxs-lookup"><span data-stu-id="4100d-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4100d-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4100d-137">Remarks</span></span>

<span data-ttu-id="4100d-138">**Ивмпсеттингс. идентично** — это свойство в Visual Basic, которое принимает параметр.</span><span class="sxs-lookup"><span data-stu-id="4100d-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="4100d-139">В C# он называется **ивмпсеттингс. Get \_ тождественным** методом.</span><span class="sxs-lookup"><span data-stu-id="4100d-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="4100d-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="4100d-140">Examples</span></span>

<span data-ttu-id="4100d-141">В следующем примере каждый из свойств **ивмпсеттингс** проверяется с помощью свойства **Available** (метод **Get- \_ Available** в C#).</span><span class="sxs-lookup"><span data-stu-id="4100d-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="4100d-142">Имя свойства и результат каждого теста отображаются в многострочном текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="4100d-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="4100d-143">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="4100d-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="4100d-144">Требования</span><span class="sxs-lookup"><span data-stu-id="4100d-144">Requirements</span></span>



| <span data-ttu-id="4100d-145">Требование</span><span class="sxs-lookup"><span data-stu-id="4100d-145">Requirement</span></span> | <span data-ttu-id="4100d-146">Значение</span><span class="sxs-lookup"><span data-stu-id="4100d-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4100d-147">Версия</span><span class="sxs-lookup"><span data-stu-id="4100d-147">Version</span></span><br/>   | <span data-ttu-id="4100d-148">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4100d-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4100d-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4100d-149">Namespace</span></span><br/> | <span data-ttu-id="4100d-150">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4100d-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4100d-151">Сборка</span><span class="sxs-lookup"><span data-stu-id="4100d-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4100d-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4100d-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4100d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4100d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4100d-154">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-155">**Ивмпсеттингс. Автозапуск (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-156">**Ивмпсеттингс. Balance (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-157">**Ивмпсеттингс. baseURL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-158">**Ивмпсеттингс. Дефаултфраме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-159">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-160">**Ивмпсеттингс. мода (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-161">**Ивмпсеттингс. Инвокеурлс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-162">**Ивмпсеттингс. выкл. (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-163">**Ивмпсеттингс. Плайкаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-164">**Ивмпсеттингс. rate (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-165">**Ивмпсеттингс. setMode (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4100d-166">**Ивмпсеттингс. Volume (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4100d-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





