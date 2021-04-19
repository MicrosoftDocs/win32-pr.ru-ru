---
title: Ивмпнетворк Сетпроксипорт, метод
description: Метод Сетпроксипорт указывает используемый порт прокси-сервера. | Ивмпнетворк Сетпроксипорт, метод
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- Сетпроксипорт метод Windows Media Player
- Сетпроксипорт метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Сетпроксипорт
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708470"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="dfe80-107">Метод Ивмпнетворк:: Сетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="dfe80-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="dfe80-108">Метод **сетпроксипорт** указывает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="dfe80-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe80-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfe80-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="dfe80-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfe80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe80-111">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfe80-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfe80-112">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="dfe80-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="dfe80-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="dfe80-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfe80-114">*лпроксипорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfe80-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfe80-115">Объект **System. Int32** , который является портом прокси-сервера для использования.</span><span class="sxs-lookup"><span data-stu-id="dfe80-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfe80-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfe80-116">Return value</span></span>

<span data-ttu-id="dfe80-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dfe80-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfe80-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfe80-118">Remarks</span></span>

<span data-ttu-id="dfe80-119">Этот метод не действует, если значение, полученное из **ивмпнетворк. жетпроксисеттингс** , равно 2 (используйте параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="dfe80-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="dfe80-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="dfe80-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="dfe80-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="dfe80-121">Examples</span></span>

<span data-ttu-id="dfe80-122">В следующем примере кода используется **сетпроксипорт** для указания номера порта прокси-сервера проигрывателя Windows Media для протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="dfe80-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="dfe80-123">Номер порта извлекается из текстового поля при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="dfe80-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="dfe80-124">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="dfe80-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="dfe80-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dfe80-125">Requirements</span></span>



| <span data-ttu-id="dfe80-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dfe80-126">Requirement</span></span> | <span data-ttu-id="dfe80-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dfe80-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe80-128">Версия</span><span class="sxs-lookup"><span data-stu-id="dfe80-128">Version</span></span><br/>   | <span data-ttu-id="dfe80-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dfe80-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dfe80-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dfe80-130">Namespace</span></span><br/> | <span data-ttu-id="dfe80-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="dfe80-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dfe80-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="dfe80-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dfe80-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe80-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe80-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfe80-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe80-135">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dfe80-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfe80-136">**Ивмпнетворк. Жетпроксипорт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dfe80-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfe80-137">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dfe80-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





