---
title: Ивмпнетворк Сетпроксексцептионлист, метод
description: Метод Сетпроксексцептионлист задает список исключений прокси-сервера. | Ивмпнетворк Сетпроксексцептионлист, метод
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- Сетпроксексцептионлист метод Windows Media Player
- Сетпроксексцептионлист метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Сетпроксексцептионлист
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689528"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="afbb0-107">Метод Ивмпнетворк:: Сетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="afbb0-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="afbb0-108">Метод **сетпроксексцептионлист** задает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="afbb0-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="afbb0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afbb0-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="afbb0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="afbb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afbb0-111">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afbb0-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afbb0-112">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="afbb0-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="afbb0-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="afbb0-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="afbb0-114">*пбстрексцептионлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afbb0-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afbb0-115">**Строка System. String** , которая представляет собой разделенный точками с запятой список узлов, для которых прокси-сервер пропускается.</span><span class="sxs-lookup"><span data-stu-id="afbb0-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="afbb0-116">Начальные и конечные пробелы не должны присутствовать.</span><span class="sxs-lookup"><span data-stu-id="afbb0-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afbb0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afbb0-117">Return value</span></span>

<span data-ttu-id="afbb0-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="afbb0-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="afbb0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afbb0-119">Remarks</span></span>

<span data-ttu-id="afbb0-120">Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.</span><span class="sxs-lookup"><span data-stu-id="afbb0-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="afbb0-121">\*Символ может использоваться в качестве подстановочного знака для записи списка.</span><span class="sxs-lookup"><span data-stu-id="afbb0-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="afbb0-122">Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.</span><span class="sxs-lookup"><span data-stu-id="afbb0-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="afbb0-123">Этот метод не действует, если значение, полученное из **ивмпнетворк. жетпроксисеттингс** , равно 2 (используйте параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="afbb0-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="afbb0-124">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="afbb0-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="afbb0-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="afbb0-125">Examples</span></span>

<span data-ttu-id="afbb0-126">В следующем примере кода используется **сетпроксексцептионлист** для указания списка узлов, для которых прокси-сервер пропускается при использовании протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="afbb0-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="afbb0-127">Новый список извлекается из текстового поля при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="afbb0-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="afbb0-128">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="afbb0-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="afbb0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="afbb0-129">Requirements</span></span>



| <span data-ttu-id="afbb0-130">Требование</span><span class="sxs-lookup"><span data-stu-id="afbb0-130">Requirement</span></span> | <span data-ttu-id="afbb0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="afbb0-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afbb0-132">Версия</span><span class="sxs-lookup"><span data-stu-id="afbb0-132">Version</span></span><br/>   | <span data-ttu-id="afbb0-133">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="afbb0-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="afbb0-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="afbb0-134">Namespace</span></span><br/> | <span data-ttu-id="afbb0-135">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="afbb0-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="afbb0-136">Сборка</span><span class="sxs-lookup"><span data-stu-id="afbb0-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="afbb0-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="afbb0-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afbb0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afbb0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afbb0-139">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="afbb0-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="afbb0-140">**Ивмпнетворк. Жетпроксексцептионлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="afbb0-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="afbb0-141">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="afbb0-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





