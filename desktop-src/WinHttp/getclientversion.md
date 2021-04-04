---
description: Возвращает версию обработчика обработки WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: Функция Жетклиентверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910848"
---
# <a name="getclientversion-function"></a><span data-ttu-id="b48e1-103">Функция Жетклиентверсион</span><span class="sxs-lookup"><span data-stu-id="b48e1-103">getClientVersion function</span></span>

<span data-ttu-id="b48e1-104">Возвращает версию обработчика обработки WPAD.</span><span class="sxs-lookup"><span data-stu-id="b48e1-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="b48e1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b48e1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48e1-106">*ипаддресслист*</span><span class="sxs-lookup"><span data-stu-id="b48e1-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="b48e1-107">Строка, разделенная точкой с запятой, содержащая IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b48e1-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b48e1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b48e1-108">Return value</span></span>

<span data-ttu-id="b48e1-109">Список упорядоченных IP-адресов, разделенных точкой с запятой, или пустая строка, если не удалось отсортировать список IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b48e1-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="b48e1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b48e1-110">Remarks</span></span>

<span data-ttu-id="b48e1-111">В настоящее время эта функция возвращает версию 1,0.</span><span class="sxs-lookup"><span data-stu-id="b48e1-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="b48e1-112">Корпорация Майкрософт добавила эту функцию, чтобы позволить ИТ-администраторам обновлять свои скрипты WPAD, чтобы использовать разные версии механизма обработки WPAD, не нарушая их существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="b48e1-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="b48e1-113">Например, если корпорация Майкрософт добавила функцию в версию 2,0 модуля WPAD, администраторы смогут проверить версию, прежде чем пытаться вызвать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b48e1-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="b48e1-114">Это позволяет сценарию работать с клиентами, работающими под управлением версий 1,0 и 2,0 модуля WPAD.</span><span class="sxs-lookup"><span data-stu-id="b48e1-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="b48e1-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="b48e1-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="b48e1-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b48e1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48e1-117">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="b48e1-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="b48e1-118">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="b48e1-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



