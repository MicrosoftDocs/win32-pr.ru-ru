---
title: Ивмпнетворк Жетпроксинаме, метод
description: Метод Жетпроксинаме возвращает имя используемого прокси-сервера.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- Жетпроксинаме метод Windows Media Player
- Жетпроксинаме метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксинаме
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665163"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="2cbfa-106">Метод Ивмпнетворк:: Жетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="2cbfa-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="2cbfa-107">Метод **жетпроксинаме** возвращает имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbfa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbfa-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="2cbfa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cbfa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbfa-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cbfa-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbfa-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="2cbfa-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="2cbfa-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbfa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cbfa-113">Return value</span></span>

<span data-ttu-id="2cbfa-114">**Строка System. String** , которая является именем используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="2cbfa-115">Значение имеет смысл только в том случае, если **ивмпнетворк. жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="2cbfa-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbfa-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbfa-116">Remarks</span></span>

<span data-ttu-id="2cbfa-117">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="2cbfa-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="2cbfa-118">Examples</span></span>

<span data-ttu-id="2cbfa-119">В следующем примере кода используется **жетпроксинаме** для вывода имен прокси-сервера проигрывателя Windows Media для протоколов HTTP и MMS.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="2cbfa-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2cbfa-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="2cbfa-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbfa-121">Requirements</span></span>



| <span data-ttu-id="2cbfa-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbfa-122">Requirement</span></span> | <span data-ttu-id="2cbfa-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbfa-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbfa-124">Версия</span><span class="sxs-lookup"><span data-stu-id="2cbfa-124">Version</span></span><br/>   | <span data-ttu-id="2cbfa-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2cbfa-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2cbfa-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2cbfa-126">Namespace</span></span><br/> | <span data-ttu-id="2cbfa-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2cbfa-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2cbfa-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="2cbfa-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2cbfa-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2cbfa-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbfa-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cbfa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbfa-131">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2cbfa-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cbfa-132">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2cbfa-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cbfa-133">**Ивмпнетворк. Сетпроксинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2cbfa-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





