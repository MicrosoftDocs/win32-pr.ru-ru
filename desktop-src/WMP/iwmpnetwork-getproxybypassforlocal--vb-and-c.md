---
title: Ивмпнетворк Жетпроксибипассфорлокал, метод
description: Метод Жетпроксибипассфорлокал возвращает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- Жетпроксибипассфорлокал метод Windows Media Player
- Жетпроксибипассфорлокал метод проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, метод Жетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688788"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="b7b6e-106">Метод Ивмпнетворк:: Жетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="b7b6e-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="b7b6e-107">Метод **жетпроксибипассфорлокал** возвращает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b6e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7b6e-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="b7b6e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7b6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b6e-110">*бстрпротокол*</span><span class="sxs-lookup"><span data-stu-id="b7b6e-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b6e-111">**Строка System. String** , которая является именем протокола.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b6e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7b6e-112">Return value</span></span>

<span data-ttu-id="b7b6e-113">Значение **System. Boolean** , указывающее, пропускается ли прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="b7b6e-114">Значение имеет смысл только в том случае, если **ивмпнетворк. жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="b7b6e-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b6e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7b6e-115">Remarks</span></span>

<span data-ttu-id="b7b6e-116">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="b7b6e-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="b7b6e-117">Examples</span></span>

<span data-ttu-id="b7b6e-118">В следующем примере кода используется **жетпроксибипассфорлокал** , чтобы показать, настроен ли проигрыватель Windows Media для обхода прокси-сервера для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="b7b6e-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="b7b6e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b7b6e-120">Requirements</span></span>



| <span data-ttu-id="b7b6e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b7b6e-121">Requirement</span></span> | <span data-ttu-id="b7b6e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b7b6e-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b6e-123">Версия</span><span class="sxs-lookup"><span data-stu-id="b7b6e-123">Version</span></span><br/>   | <span data-ttu-id="b7b6e-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b7b6e-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="b7b6e-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7b6e-125">Namespace</span></span><br/> | <span data-ttu-id="b7b6e-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b7b6e-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="b7b6e-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="b7b6e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b7b6e-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b6e-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b6e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7b6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b6e-130">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b7b6e-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b7b6e-131">**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b7b6e-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b7b6e-132">**Ивмпнетворк. Сетпроксибипассфорлокал (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b7b6e-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





