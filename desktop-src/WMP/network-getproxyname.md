---
title: Метод Network. Жетпроксинаме
description: Метод Жетпроксинаме извлекает имя используемого прокси-сервера.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- Жетпроксинаме метод Windows Media Player
- Жетпроксинаме метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксинаме
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704463"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="709b8-106">Метод Network. Жетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="709b8-106">Network.getProxyName method</span></span>

<span data-ttu-id="709b8-107">Метод **жетпроксинаме** извлекает имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="709b8-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="709b8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="709b8-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="709b8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="709b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="709b8-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="709b8-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="709b8-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="709b8-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="709b8-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="709b8-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="709b8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="709b8-113">Return value</span></span>

<span data-ttu-id="709b8-114">Этот метод возвращает **строку** , содержащую имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="709b8-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="709b8-115">Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="709b8-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="709b8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="709b8-116">Remarks</span></span>

<span data-ttu-id="709b8-117">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="709b8-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="709b8-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="709b8-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="709b8-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="709b8-119">Examples</span></span>

<span data-ttu-id="709b8-120">В следующем примере JScript используется *Network*. **жетпроксинаме** для вывода имен прокси-сервера проигрывателя Windows Media для протоколов HTTP и MMS.</span><span class="sxs-lookup"><span data-stu-id="709b8-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="709b8-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="709b8-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="709b8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="709b8-122">Requirements</span></span>



| <span data-ttu-id="709b8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="709b8-123">Requirement</span></span> | <span data-ttu-id="709b8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="709b8-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="709b8-125">Версия</span><span class="sxs-lookup"><span data-stu-id="709b8-125">Version</span></span><br/> | <span data-ttu-id="709b8-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="709b8-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="709b8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="709b8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="709b8-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="709b8-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709b8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="709b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709b8-130">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="709b8-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="709b8-131">**Network. Жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="709b8-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





