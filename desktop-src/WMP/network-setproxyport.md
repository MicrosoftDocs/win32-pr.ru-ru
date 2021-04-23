---
title: Метод Network. Сетпроксипорт
description: Метод Сетпроксипорт указывает используемый порт прокси-сервера. | Метод Network. Сетпроксипорт
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Сетпроксипорт метод Windows Media Player
- Сетпроксипорт метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксипорт
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694402"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="143ea-107">Метод Network. Сетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="143ea-107">Network.setProxyPort method</span></span>

<span data-ttu-id="143ea-108">Метод **сетпроксипорт** указывает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="143ea-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="143ea-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="143ea-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="143ea-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="143ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143ea-111">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="143ea-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="143ea-112">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="143ea-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="143ea-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="143ea-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="143ea-114">*порт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="143ea-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="143ea-115">**Число** (**длинное**), определяющее используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="143ea-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="143ea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="143ea-116">Return value</span></span>

<span data-ttu-id="143ea-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="143ea-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="143ea-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="143ea-118">Remarks</span></span>

<span data-ttu-id="143ea-119">Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="143ea-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="143ea-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="143ea-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="143ea-121">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="143ea-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="143ea-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="143ea-122">Examples</span></span>

<span data-ttu-id="143ea-123">В следующем примере JScript используется *Network*. **сетпроксипорт** , чтобы указать номер порта прокси-сервера проигрывателя Windows Media для протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="143ea-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="143ea-124">Номер порта извлекается из HTML-элемента ввода с идентификатором ID = "PORT".</span><span class="sxs-lookup"><span data-stu-id="143ea-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="143ea-125">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="143ea-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="143ea-126">Требования</span><span class="sxs-lookup"><span data-stu-id="143ea-126">Requirements</span></span>



| <span data-ttu-id="143ea-127">Требование</span><span class="sxs-lookup"><span data-stu-id="143ea-127">Requirement</span></span> | <span data-ttu-id="143ea-128">Значение</span><span class="sxs-lookup"><span data-stu-id="143ea-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="143ea-129">Версия</span><span class="sxs-lookup"><span data-stu-id="143ea-129">Version</span></span><br/> | <span data-ttu-id="143ea-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="143ea-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="143ea-131">DLL</span><span class="sxs-lookup"><span data-stu-id="143ea-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="143ea-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="143ea-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="143ea-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="143ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143ea-134">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="143ea-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





