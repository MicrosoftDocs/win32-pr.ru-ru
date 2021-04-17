---
title: Метод Network. setProxySettings
description: Метод setProxySettings указывает параметр прокси-сервера для данного протокола.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setProxySettings метод Windows Media Player
- setProxySettings метод Windows Media Player, класс Network
- Класс сети Windows Media Player, метод setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694657"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="f437d-106">Метод Network. setProxySettings</span><span class="sxs-lookup"><span data-stu-id="f437d-106">Network.setProxySettings method</span></span>

<span data-ttu-id="f437d-107">Метод **setProxySettings** указывает параметр прокси-сервера для данного протокола.</span><span class="sxs-lookup"><span data-stu-id="f437d-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f437d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f437d-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="f437d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f437d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f437d-110">*протокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f437d-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f437d-111">**Строка** , указывающая имя протокола.</span><span class="sxs-lookup"><span data-stu-id="f437d-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="f437d-112">Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f437d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f437d-113">*параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f437d-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f437d-114">**Число** (**Long**), содержащее одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f437d-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="f437d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f437d-115">Value</span></span> | <span data-ttu-id="f437d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f437d-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="f437d-117">0</span><span class="sxs-lookup"><span data-stu-id="f437d-117">0</span></span>     | <span data-ttu-id="f437d-118">Не используйте прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="f437d-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="f437d-119">1</span><span class="sxs-lookup"><span data-stu-id="f437d-119">1</span></span>     | <span data-ttu-id="f437d-120">Используйте параметры прокси-сервера текущего браузера (допустим только для HTTP).</span><span class="sxs-lookup"><span data-stu-id="f437d-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="f437d-121">2</span><span class="sxs-lookup"><span data-stu-id="f437d-121">2</span></span>     | <span data-ttu-id="f437d-122">Используйте заданные вручную параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f437d-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="f437d-123">3</span><span class="sxs-lookup"><span data-stu-id="f437d-123">3</span></span>     | <span data-ttu-id="f437d-124">Автоматическое определение параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f437d-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f437d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f437d-125">Return value</span></span>

<span data-ttu-id="f437d-126">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f437d-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f437d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f437d-127">Remarks</span></span>

<span data-ttu-id="f437d-128">Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.</span><span class="sxs-lookup"><span data-stu-id="f437d-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="f437d-129">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f437d-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f437d-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="f437d-130">Examples</span></span>

<span data-ttu-id="f437d-131">В следующем примере используется JScript с HTML-элементом SELECT, **который позволяет пользователю указать параметр прокси-сервера проигрывателя Windows Media для протокола HTTP. Объект Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="f437d-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="f437d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f437d-132">Requirements</span></span>



| <span data-ttu-id="f437d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f437d-133">Requirement</span></span> | <span data-ttu-id="f437d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f437d-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f437d-135">Версия</span><span class="sxs-lookup"><span data-stu-id="f437d-135">Version</span></span><br/> | <span data-ttu-id="f437d-136">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="f437d-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f437d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f437d-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="f437d-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f437d-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f437d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f437d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f437d-140">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="f437d-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





