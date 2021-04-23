---
title: Ивмпнетворк Сетпроксибипассфорлокал, метод
description: Метод Сетпроксибипассфорлокал указывает, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- Сетпроксибипассфорлокал метод Windows Media Player
- Сетпроксибипассфорлокал метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Сетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704486"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="3b053-106">Метод Ивмпнетворк:: Сетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="3b053-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="3b053-107">Метод **сетпроксибипассфорлокал** указывает, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="3b053-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b053-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b053-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="3b053-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b053-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b053-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b053-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b053-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="3b053-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="3b053-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="3b053-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b053-113">*фбипассфорлокал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3b053-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b053-114">Значение **System. Boolean** , указывающее, пропускается ли прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="3b053-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b053-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b053-115">Return value</span></span>

<span data-ttu-id="3b053-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3b053-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b053-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b053-117">Remarks</span></span>

<span data-ttu-id="3b053-118">Этот метод не действует, если значение, полученное из **ивмпнетворк. жетпроксисеттингс** , равно 2 (используйте параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="3b053-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="3b053-119">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="3b053-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="3b053-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="3b053-120">Examples</span></span>

<span data-ttu-id="3b053-121">В следующем примере кода используется **сетпроксибипассфорлокал** , чтобы указать, пропускается ли прокси-сервер проигрывателя Windows Media при использовании протокола MMS, если сервер-источник находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="3b053-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="3b053-122">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="3b053-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="3b053-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3b053-123">Requirements</span></span>



| <span data-ttu-id="3b053-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3b053-124">Requirement</span></span> | <span data-ttu-id="3b053-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3b053-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b053-126">Версия</span><span class="sxs-lookup"><span data-stu-id="3b053-126">Version</span></span><br/>   | <span data-ttu-id="3b053-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3b053-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3b053-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b053-128">Namespace</span></span><br/> | <span data-ttu-id="3b053-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3b053-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b053-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="3b053-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3b053-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3b053-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b053-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b053-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b053-133">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b053-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b053-134">**Ивмпнетворк. Жетпроксибипассфорлокал (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b053-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b053-135">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b053-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





