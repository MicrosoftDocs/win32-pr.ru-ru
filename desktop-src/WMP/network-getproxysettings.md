---
title: Метод Network. Жетпроксисеттингс
description: Метод Жетпроксисеттингс извлекает параметр прокси-сервера для данного протокола.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Жетпроксисеттингс метод Windows Media Player
- Жетпроксисеттингс метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод Жетпроксисеттингс
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648759"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="17931-106">Метод Network. Жетпроксисеттингс</span><span class="sxs-lookup"><span data-stu-id="17931-106">Network.getProxySettings method</span></span>

<span data-ttu-id="17931-107">Метод **жетпроксисеттингс** извлекает параметр прокси-сервера для данного протокола.</span><span class="sxs-lookup"><span data-stu-id="17931-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="17931-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17931-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="17931-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="17931-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17931-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17931-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17931-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="17931-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="17931-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="17931-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17931-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17931-113">Return value</span></span>

<span data-ttu-id="17931-114">Этот метод возвращает **число** (**Long**), содержащее одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="17931-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="17931-115">Значение</span><span class="sxs-lookup"><span data-stu-id="17931-115">Value</span></span> | <span data-ttu-id="17931-116">Описание</span><span class="sxs-lookup"><span data-stu-id="17931-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="17931-117">0</span><span class="sxs-lookup"><span data-stu-id="17931-117">0</span></span>     | <span data-ttu-id="17931-118">Прокси-сервер не используется.</span><span class="sxs-lookup"><span data-stu-id="17931-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="17931-119">1</span><span class="sxs-lookup"><span data-stu-id="17931-119">1</span></span>     | <span data-ttu-id="17931-120">Используются параметры прокси-сервера для текущего браузера (допустимы только для HTTP).</span><span class="sxs-lookup"><span data-stu-id="17931-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="17931-121">2</span><span class="sxs-lookup"><span data-stu-id="17931-121">2</span></span>     | <span data-ttu-id="17931-122">Используются заданные вручную параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="17931-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="17931-123">3</span><span class="sxs-lookup"><span data-stu-id="17931-123">3</span></span>     | <span data-ttu-id="17931-124">Параметры прокси-сервера обнаруживаются в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="17931-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="17931-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17931-125">Remarks</span></span>

<span data-ttu-id="17931-126">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="17931-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="17931-127">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="17931-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="17931-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="17931-128">Examples</span></span>

<span data-ttu-id="17931-129">В следующем примере JScript используется *Network*. **жетпроксисеттингс** для вывода сообщения, которое предоставляет сведения о текущих параметрах прокси-сервера проигрывателя в окне браузера.</span><span class="sxs-lookup"><span data-stu-id="17931-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="17931-130">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="17931-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="17931-131">Требования</span><span class="sxs-lookup"><span data-stu-id="17931-131">Requirements</span></span>



| <span data-ttu-id="17931-132">Требование</span><span class="sxs-lookup"><span data-stu-id="17931-132">Requirement</span></span> | <span data-ttu-id="17931-133">Значение</span><span class="sxs-lookup"><span data-stu-id="17931-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17931-134">Версия</span><span class="sxs-lookup"><span data-stu-id="17931-134">Version</span></span><br/> | <span data-ttu-id="17931-135">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="17931-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="17931-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17931-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="17931-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17931-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17931-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17931-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17931-139">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="17931-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





