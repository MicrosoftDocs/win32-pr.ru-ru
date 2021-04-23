---
title: Ивмпнетворк Жетпроксексцептионлист, метод
description: Метод Жетпроксексцептионлист возвращает список исключений прокси-сервера.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- Жетпроксексцептионлист метод Windows Media Player
- Жетпроксексцептионлист метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксексцептионлист
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665164"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="ca283-106">Метод Ивмпнетворк:: Жетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="ca283-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="ca283-107">Метод **жетпроксексцептионлист** возвращает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ca283-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca283-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca283-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="ca283-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca283-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca283-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca283-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca283-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="ca283-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="ca283-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ca283-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca283-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca283-113">Return value</span></span>

<span data-ttu-id="ca283-114">**Строка System. String** , которая представляет собой разделенный точками с запятой список узлов, для которых прокси-сервер пропускается.</span><span class="sxs-lookup"><span data-stu-id="ca283-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="ca283-115">Значение имеет смысл только в том случае, если **ивмпнетворк. жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="ca283-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca283-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca283-116">Remarks</span></span>

<span data-ttu-id="ca283-117">Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.</span><span class="sxs-lookup"><span data-stu-id="ca283-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="ca283-118">\*Символ может использоваться в качестве подстановочного знака для записи списка.</span><span class="sxs-lookup"><span data-stu-id="ca283-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="ca283-119">Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.</span><span class="sxs-lookup"><span data-stu-id="ca283-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="ca283-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="ca283-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="ca283-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="ca283-121">Examples</span></span>

<span data-ttu-id="ca283-122">В следующем примере кода используется **жетпроксексцептионлист** , чтобы показать, настроен ли проигрыватель Windows Media для обхода прокси-сервера для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="ca283-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="ca283-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="ca283-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="ca283-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ca283-124">Requirements</span></span>



| <span data-ttu-id="ca283-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ca283-125">Requirement</span></span> | <span data-ttu-id="ca283-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ca283-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca283-127">Версия</span><span class="sxs-lookup"><span data-stu-id="ca283-127">Version</span></span><br/>   | <span data-ttu-id="ca283-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ca283-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ca283-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca283-129">Namespace</span></span><br/> | <span data-ttu-id="ca283-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="ca283-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ca283-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="ca283-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ca283-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ca283-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca283-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca283-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca283-134">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ca283-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ca283-135">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ca283-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ca283-136">**Ивмпнетворк. Сетпроксексцептионлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ca283-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





