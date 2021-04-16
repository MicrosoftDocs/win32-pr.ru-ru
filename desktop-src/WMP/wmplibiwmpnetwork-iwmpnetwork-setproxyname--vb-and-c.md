---
title: Ивмпнетворк Сетпроксинаме, метод
description: Метод Сетпроксинаме указывает имя прокси-сервера для использования. | Ивмпнетворк Сетпроксинаме, метод
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- Сетпроксинаме метод Windows Media Player
- Сетпроксинаме метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Сетпроксинаме
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649118"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="3a9a2-107">Метод Ивмпнетворк:: Сетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="3a9a2-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="3a9a2-108">Метод **сетпроксинаме** указывает имя прокси-сервера для использования.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a9a2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a9a2-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="3a9a2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a9a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a9a2-111">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a9a2-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a9a2-112">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="3a9a2-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="3a9a2-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9a2-114">*бстрпроксинаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a9a2-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a9a2-115">**Строка System. String** , которая является именем используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a9a2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a9a2-116">Return value</span></span>

<span data-ttu-id="3a9a2-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a9a2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a9a2-118">Remarks</span></span>

<span data-ttu-id="3a9a2-119">Этот метод не действует, если значение, полученное из **ивмпнетворк. жетпроксисеттингс** , равно 2 (используйте параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="3a9a2-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="3a9a2-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="3a9a2-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="3a9a2-121">Examples</span></span>

<span data-ttu-id="3a9a2-122">В следующем примере кода используется **сетпроксинаме** для указания имени прокси-сервера проигрывателя Windows Media для протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="3a9a2-123">При нажатии кнопки новое имя извлекается из текстового поля.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="3a9a2-124">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="3a9a2-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3a9a2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3a9a2-125">Requirements</span></span>



| <span data-ttu-id="3a9a2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3a9a2-126">Requirement</span></span> | <span data-ttu-id="3a9a2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3a9a2-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9a2-128">Версия</span><span class="sxs-lookup"><span data-stu-id="3a9a2-128">Version</span></span><br/>   | <span data-ttu-id="3a9a2-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3a9a2-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3a9a2-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a9a2-130">Namespace</span></span><br/> | <span data-ttu-id="3a9a2-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3a9a2-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3a9a2-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="3a9a2-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a9a2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a9a2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a9a2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a9a2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a9a2-135">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a9a2-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a9a2-136">**Ивмпнетворк. Жетпроксинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a9a2-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a9a2-137">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a9a2-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





