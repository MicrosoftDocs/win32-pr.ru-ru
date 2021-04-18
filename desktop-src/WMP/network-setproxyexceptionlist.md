---
title: Метод Network. Сетпроксексцептионлист
description: Метод Сетпроксексцептионлист задает список исключений прокси-сервера. | Метод Network. Сетпроксексцептионлист
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Сетпроксексцептионлист метод Windows Media Player
- Сетпроксексцептионлист метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксексцептионлист
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694446"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="77f2a-107">Метод Network. Сетпроксексцептионлист</span><span class="sxs-lookup"><span data-stu-id="77f2a-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="77f2a-108">Метод **сетпроксексцептионлист** задает список исключений прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="77f2a-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f2a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77f2a-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="77f2a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="77f2a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f2a-111">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77f2a-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77f2a-112">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="77f2a-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="77f2a-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="77f2a-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="77f2a-114">*список* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77f2a-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77f2a-115">**Строка** , указывающая список узлов, разделенных точкой с запятой, для которых прокси-сервер пропускается.</span><span class="sxs-lookup"><span data-stu-id="77f2a-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f2a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77f2a-116">Return value</span></span>

<span data-ttu-id="77f2a-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="77f2a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77f2a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77f2a-118">Remarks</span></span>

<span data-ttu-id="77f2a-119">Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.</span><span class="sxs-lookup"><span data-stu-id="77f2a-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="77f2a-120">\*Символ может использоваться в качестве подстановочного знака для списка записей.</span><span class="sxs-lookup"><span data-stu-id="77f2a-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="77f2a-121">Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.</span><span class="sxs-lookup"><span data-stu-id="77f2a-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="77f2a-122">Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="77f2a-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="77f2a-123">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="77f2a-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="77f2a-124">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="77f2a-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="77f2a-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="77f2a-125">Examples</span></span>

<span data-ttu-id="77f2a-126">В следующем примере JScript используется *Network*. **сетпроксексцептионлист** , чтобы указать список узлов, для которых прокси-сервер пропускается при использовании протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="77f2a-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="77f2a-127">Новый список извлекается из ТЕКСТОВОГО HTML-элемента с идентификатором ID = "КСЛИСТ".</span><span class="sxs-lookup"><span data-stu-id="77f2a-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="77f2a-128">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="77f2a-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="77f2a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="77f2a-129">Requirements</span></span>



| <span data-ttu-id="77f2a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="77f2a-130">Requirement</span></span> | <span data-ttu-id="77f2a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="77f2a-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77f2a-132">Версия</span><span class="sxs-lookup"><span data-stu-id="77f2a-132">Version</span></span><br/> | <span data-ttu-id="77f2a-133">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="77f2a-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="77f2a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="77f2a-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="77f2a-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77f2a-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f2a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77f2a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f2a-137">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="77f2a-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





