---
description: Указывает, будет ли устройство мобильной широкополосной связи автоматически подключаться к сети.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Аутоконнектонинтернет (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263178"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="9954f-103">Аутоконнектонинтернет (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="9954f-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="9954f-104">Элемент **аутоконнектонинтернет (мбнпрофиле)** указывает, будет ли устройство мобильной широкополосной связи автоматически подключаться к сети.</span><span class="sxs-lookup"><span data-stu-id="9954f-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="9954f-105">Если задано значение **false**, логика автоматического подключения службы мобильной широкополосной связи не будет использоваться при наличии других сетевых подключений, доступных системе.</span><span class="sxs-lookup"><span data-stu-id="9954f-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="9954f-106">Если задано **значение true**, служба мобильной широкополосной связи будет пытаться автоматически подключить устройство к сети на основе параметра автоматического подключения, определенного в элементе [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9954f-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="9954f-107">**Windows 8 и более поздние версии:** Этот элемент не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="9954f-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="9954f-108">Используйте метод [**вкмсетпроперти**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) с параметром *Property* , установленным **в \_ \_ \_ \_ параметре WCM Global Property** , а не в политику.</span><span class="sxs-lookup"><span data-stu-id="9954f-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="9954f-109">Элемент **аутоконнектонинтернет** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9954f-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9954f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9954f-110">Requirements</span></span>



| <span data-ttu-id="9954f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9954f-111">Requirement</span></span> | <span data-ttu-id="9954f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9954f-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="9954f-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9954f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9954f-114">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="9954f-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="9954f-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9954f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9954f-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9954f-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="9954f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9954f-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9954f-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="9954f-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9954f-119">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="9954f-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="9954f-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="9954f-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9954f-121">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="9954f-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

