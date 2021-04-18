---
title: Метод Network. Жетпроксибипассфорлокал
description: Метод Жетпроксибипассфорлокал извлекает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Жетпроксибипассфорлокал метод Windows Media Player
- Жетпроксибипассфорлокал метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704387"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="4950d-106">Метод Network. Жетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="4950d-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="4950d-107">Метод **жетпроксибипассфорлокал** извлекает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="4950d-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="4950d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4950d-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="4950d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4950d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4950d-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4950d-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4950d-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="4950d-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="4950d-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4950d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4950d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4950d-113">Return value</span></span>

<span data-ttu-id="4950d-114">Этот метод возвращает **логическое значение** , указывающее, пропускается ли прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="4950d-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="4950d-115">Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="4950d-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="4950d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4950d-116">Remarks</span></span>

<span data-ttu-id="4950d-117">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="4950d-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="4950d-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4950d-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="4950d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4950d-119">Examples</span></span>

<span data-ttu-id="4950d-120">В следующем примере JScript используется *Network*. **жетпроксибипассфорлокал** , чтобы отобразить, настроен ли проигрыватель Windows Media на обход прокси-сервера для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="4950d-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="4950d-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="4950d-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="4950d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4950d-122">Requirements</span></span>



| <span data-ttu-id="4950d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4950d-123">Requirement</span></span> | <span data-ttu-id="4950d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4950d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4950d-125">Версия</span><span class="sxs-lookup"><span data-stu-id="4950d-125">Version</span></span><br/> | <span data-ttu-id="4950d-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4950d-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4950d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4950d-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="4950d-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4950d-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4950d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4950d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4950d-130">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="4950d-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4950d-131">**Network. Жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="4950d-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





