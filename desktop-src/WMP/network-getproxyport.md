---
title: Метод Network. Жетпроксипорт
description: Метод Жетпроксипорт извлекает используемый порт прокси-сервера.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- Жетпроксипорт метод Windows Media Player
- Жетпроксипорт метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксипорт
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704237"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="17ba6-106">Метод Network. Жетпроксипорт</span><span class="sxs-lookup"><span data-stu-id="17ba6-106">Network.getProxyPort method</span></span>

<span data-ttu-id="17ba6-107">Метод **жетпроксипорт** извлекает используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="17ba6-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ba6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17ba6-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="17ba6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="17ba6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ba6-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17ba6-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ba6-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="17ba6-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="17ba6-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="17ba6-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ba6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17ba6-113">Return value</span></span>

<span data-ttu-id="17ba6-114">Этот метод возвращает **число** (**Long**), содержащее используемый порт прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="17ba6-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="17ba6-115">Возвращаемое значение имеет смысл только в том случае, если **жетпроксисеттингс** возвращает значение 2 (использовать параметры вручную).</span><span class="sxs-lookup"><span data-stu-id="17ba6-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="17ba6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17ba6-116">Remarks</span></span>

<span data-ttu-id="17ba6-117">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="17ba6-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="17ba6-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="17ba6-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="17ba6-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="17ba6-119">Examples</span></span>

<span data-ttu-id="17ba6-120">В следующем примере JScript используется *Network*. **жетпроксипорт** для вывода текущих номеров портов прокси-сервера проигрывателя Windows Media для протоколов MMS и HTTP.</span><span class="sxs-lookup"><span data-stu-id="17ba6-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="17ba6-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="17ba6-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="17ba6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="17ba6-122">Requirements</span></span>



| <span data-ttu-id="17ba6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="17ba6-123">Requirement</span></span> | <span data-ttu-id="17ba6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="17ba6-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17ba6-125">Версия</span><span class="sxs-lookup"><span data-stu-id="17ba6-125">Version</span></span><br/> | <span data-ttu-id="17ba6-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="17ba6-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="17ba6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="17ba6-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="17ba6-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ba6-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ba6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17ba6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ba6-130">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="17ba6-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="17ba6-131">**Network. Жетпроксисеттингс**</span><span class="sxs-lookup"><span data-stu-id="17ba6-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





