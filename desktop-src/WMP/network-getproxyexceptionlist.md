---
title: Метод Network. Жетпроксексцептионлист
description: Метод Жетпроксексцептионлист извлекает список исключений прокси-сервера.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- Жетпроксексцептионлист метод Windows Media Player
- Жетпроксексцептионлист метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксексцептионлист
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708491"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="f4274-106">Метод Network. Жетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="f4274-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="f4274-107">Метод **жетпроксексцептионлист** извлекает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f4274-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4274-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4274-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="f4274-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4274-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4274-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4274-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4274-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="f4274-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="f4274-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f4274-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4274-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4274-113">Return value</span></span>

<span data-ttu-id="f4274-114">Этот метод возвращает **строку** , указывающую список узлов, разделенных точкой с запятой, для которых прокси-сервер пропускается.</span><span class="sxs-lookup"><span data-stu-id="f4274-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="f4274-115">Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="f4274-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4274-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4274-116">Remarks</span></span>

<span data-ttu-id="f4274-117">Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.</span><span class="sxs-lookup"><span data-stu-id="f4274-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="f4274-118">\*Символ может использоваться в качестве подстановочного знака для списка записей.</span><span class="sxs-lookup"><span data-stu-id="f4274-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="f4274-119">Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.</span><span class="sxs-lookup"><span data-stu-id="f4274-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="f4274-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="f4274-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="f4274-121">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f4274-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f4274-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="f4274-122">Examples</span></span>

<span data-ttu-id="f4274-123">В следующем примере JScript используется *Network*. **жетпроксексцептионлист** для вывода списка пропущенных прокси-серверов для протоколов MMS и HTTP.</span><span class="sxs-lookup"><span data-stu-id="f4274-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="f4274-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="f4274-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="f4274-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f4274-125">Requirements</span></span>



| <span data-ttu-id="f4274-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f4274-126">Requirement</span></span> | <span data-ttu-id="f4274-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f4274-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4274-128">Версия</span><span class="sxs-lookup"><span data-stu-id="f4274-128">Version</span></span><br/> | <span data-ttu-id="f4274-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="f4274-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f4274-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f4274-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f4274-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4274-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4274-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4274-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4274-133">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="f4274-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="f4274-134">**Network. Жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="f4274-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





