---
title: Метод Network. Сетпроксинаме
description: Метод Сетпроксинаме указывает имя прокси-сервера для использования. | Метод Network. Сетпроксинаме
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Сетпроксинаме метод Windows Media Player
- Сетпроксинаме метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Сетпроксинаме
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695149"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="31572-107">Метод Network. Сетпроксинаме</span><span class="sxs-lookup"><span data-stu-id="31572-107">Network.setProxyName method</span></span>

<span data-ttu-id="31572-108">Метод **сетпроксинаме** указывает имя прокси-сервера для использования.</span><span class="sxs-lookup"><span data-stu-id="31572-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="31572-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31572-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="31572-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="31572-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31572-111">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31572-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31572-112">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="31572-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="31572-113">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="31572-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="31572-114">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31572-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31572-115">**Строка** , указывающая имя используемого прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="31572-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31572-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31572-116">Return value</span></span>

<span data-ttu-id="31572-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="31572-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31572-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31572-118">Remarks</span></span>

<span data-ttu-id="31572-119">Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="31572-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="31572-120">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="31572-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="31572-121">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="31572-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="31572-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="31572-122">Examples</span></span>

<span data-ttu-id="31572-123">В следующем примере JScript используется *Network*. **сетпроксинаме** , чтобы указать имя прокси-сервера проигрывателя Windows Media для протокола MMS.</span><span class="sxs-lookup"><span data-stu-id="31572-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="31572-124">Новое имя извлекается из ТЕКСТОВОГО элемента HTML с идентификатором ID = "имя".</span><span class="sxs-lookup"><span data-stu-id="31572-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="31572-125">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="31572-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="31572-126">Требования</span><span class="sxs-lookup"><span data-stu-id="31572-126">Requirements</span></span>



| <span data-ttu-id="31572-127">Требование</span><span class="sxs-lookup"><span data-stu-id="31572-127">Requirement</span></span> | <span data-ttu-id="31572-128">Значение</span><span class="sxs-lookup"><span data-stu-id="31572-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31572-129">Версия</span><span class="sxs-lookup"><span data-stu-id="31572-129">Version</span></span><br/> | <span data-ttu-id="31572-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="31572-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="31572-131">DLL</span><span class="sxs-lookup"><span data-stu-id="31572-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="31572-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31572-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31572-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31572-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31572-134">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="31572-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





