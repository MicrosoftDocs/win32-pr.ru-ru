---
title: Ивмпнетворк Жетпроксипорт, метод
description: Метод Жетпроксипорт Возвращает используемый порт прокси-сервера.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- Жетпроксипорт метод Windows Media Player
- Жетпроксипорт метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксипорт
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668851"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="90d00-106">Метод Ивмпнетворк:: Жетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="90d00-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="90d00-107">Метод **жетпроксипорт** Возвращает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="90d00-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d00-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90d00-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="90d00-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90d00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d00-110">*бстрпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90d00-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90d00-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="90d00-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="90d00-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="90d00-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d00-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90d00-113">Return value</span></span>

<span data-ttu-id="90d00-114">Объект **System. Int32** , который является используемым портом прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="90d00-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="90d00-115">Значение имеет смысл только в том случае, если **ивмпнетворк. жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="90d00-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="90d00-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90d00-116">Remarks</span></span>

<span data-ttu-id="90d00-117">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="90d00-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="90d00-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="90d00-118">Examples</span></span>

<span data-ttu-id="90d00-119">В следующем примере кода используется **жетпроксипорт** для вывода текущих номеров портов прокси-сервера проигрывателя Windows Media для протоколов MMS и HTTP.</span><span class="sxs-lookup"><span data-stu-id="90d00-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="90d00-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="90d00-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="90d00-121">Требования</span><span class="sxs-lookup"><span data-stu-id="90d00-121">Requirements</span></span>



| <span data-ttu-id="90d00-122">Требование</span><span class="sxs-lookup"><span data-stu-id="90d00-122">Requirement</span></span> | <span data-ttu-id="90d00-123">Значение</span><span class="sxs-lookup"><span data-stu-id="90d00-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d00-124">Версия</span><span class="sxs-lookup"><span data-stu-id="90d00-124">Version</span></span><br/>   | <span data-ttu-id="90d00-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="90d00-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="90d00-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90d00-126">Namespace</span></span><br/> | <span data-ttu-id="90d00-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="90d00-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="90d00-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="90d00-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="90d00-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="90d00-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90d00-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90d00-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d00-131">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="90d00-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d00-132">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="90d00-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90d00-133">**Ивмпнетворк. Сетпроксипорт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="90d00-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





