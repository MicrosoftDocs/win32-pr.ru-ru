---
title: Метод Network. Сетпроксибипассфорлокал
description: Метод Сетпроксибипассфорлокал задает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- Сетпроксибипассфорлокал метод Windows Media Player
- Сетпроксибипассфорлокал метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксибипассфорлокал
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695080"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="dd70b-106">Метод Network. Сетпроксибипассфорлокал</span><span class="sxs-lookup"><span data-stu-id="dd70b-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="dd70b-107">Метод **сетпроксибипассфорлокал** задает значение, указывающее, пропускается ли прокси-сервер, если исходный сервер находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd70b-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd70b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd70b-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="dd70b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd70b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd70b-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd70b-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70b-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="dd70b-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="dd70b-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="dd70b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd70b-113">*обход* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd70b-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd70b-114">**Логическое значение** , указывающее, пропускается ли прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="dd70b-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd70b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd70b-115">Return value</span></span>

<span data-ttu-id="dd70b-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd70b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd70b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd70b-117">Remarks</span></span>

<span data-ttu-id="dd70b-118">Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="dd70b-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="dd70b-119">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="dd70b-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="dd70b-120">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd70b-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="dd70b-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd70b-121">Examples</span></span>

<span data-ttu-id="dd70b-122">В следующем примере JScript используется *Network*. **сетпроксибипассфорлокал** , чтобы указать, пропускается ли прокси-сервер проигрывателя Windows Media при использовании протокола MMS, если сервер-источник находится в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd70b-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="dd70b-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="dd70b-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="dd70b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="dd70b-124">Requirements</span></span>



| <span data-ttu-id="dd70b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="dd70b-125">Requirement</span></span> | <span data-ttu-id="dd70b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="dd70b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd70b-127">Версия</span><span class="sxs-lookup"><span data-stu-id="dd70b-127">Version</span></span><br/> | <span data-ttu-id="dd70b-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="dd70b-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dd70b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dd70b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd70b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd70b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd70b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd70b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd70b-132">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="dd70b-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





