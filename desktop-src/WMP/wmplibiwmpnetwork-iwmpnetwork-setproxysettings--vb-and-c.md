---
title: Ивмпнетворк setProxySettings, метод
description: Метод setProxySettings задает параметры прокси-сервера для протокола.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- setProxySettings метод Windows Media Player
- setProxySettings метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод setProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649117"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="5f210-106">Метод Ивмпнетворк:: setProxySettings</span><span class="sxs-lookup"><span data-stu-id="5f210-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="5f210-107">Метод **setProxySettings** задает параметры прокси-сервера для протокола.</span><span class="sxs-lookup"><span data-stu-id="5f210-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f210-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f210-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="5f210-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f210-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f210-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f210-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f210-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="5f210-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="5f210-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="5f210-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f210-113">*лпроксисеттинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f210-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f210-114">Значение **System. Int32** , которое является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5f210-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="5f210-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5f210-115">Value</span></span> | <span data-ttu-id="5f210-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5f210-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="5f210-117">0</span><span class="sxs-lookup"><span data-stu-id="5f210-117">0</span></span>     | <span data-ttu-id="5f210-118">Не используйте прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="5f210-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="5f210-119">1</span><span class="sxs-lookup"><span data-stu-id="5f210-119">1</span></span>     | <span data-ttu-id="5f210-120">Используйте параметры прокси-сервера текущего браузера (допускается только для HTTP).</span><span class="sxs-lookup"><span data-stu-id="5f210-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="5f210-121">2</span><span class="sxs-lookup"><span data-stu-id="5f210-121">2</span></span>     | <span data-ttu-id="5f210-122">Используйте заданные вручную параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5f210-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="5f210-123">3</span><span class="sxs-lookup"><span data-stu-id="5f210-123">3</span></span>     | <span data-ttu-id="5f210-124">Автоматическое определение параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5f210-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f210-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f210-125">Return value</span></span>

<span data-ttu-id="5f210-126">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5f210-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f210-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f210-127">Remarks</span></span>

<span data-ttu-id="5f210-128">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="5f210-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="5f210-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="5f210-129">Examples</span></span>

<span data-ttu-id="5f210-130">В следующем примере кода используется поле со списком, позволяющее пользователю задать параметр прокси-сервера проигрывателя Windows Media для протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="5f210-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="5f210-131">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="5f210-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="5f210-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5f210-132">Requirements</span></span>



| <span data-ttu-id="5f210-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5f210-133">Requirement</span></span> | <span data-ttu-id="5f210-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5f210-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f210-135">Версия</span><span class="sxs-lookup"><span data-stu-id="5f210-135">Version</span></span><br/>   | <span data-ttu-id="5f210-136">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5f210-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5f210-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5f210-137">Namespace</span></span><br/> | <span data-ttu-id="5f210-138">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="5f210-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5f210-139">Сборка</span><span class="sxs-lookup"><span data-stu-id="5f210-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5f210-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5f210-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f210-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f210-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f210-142">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5f210-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5f210-143">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5f210-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





