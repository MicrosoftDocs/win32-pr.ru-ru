---
title: Иажентнотифисинкекс Активеклиентчанже
description: Иажентнотифисинкекс Активеклиентчанже
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700579"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="1a6e9-103">Иажентнотифисинкекс:: Активеклиентчанже</span><span class="sxs-lookup"><span data-stu-id="1a6e9-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="1a6e9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a6e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="1a6e9-105">Уведомляет клиентское приложение, если его активный клиент больше не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="1a6e9-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="1a6e9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="1a6e9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="1a6e9-108">Идентификатор символа, для которого изменилось состояние активного клиента.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="1a6e9-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*лстатус*</span><span class="sxs-lookup"><span data-stu-id="1a6e9-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="1a6e9-110">Активное изменение состояния клиента, которое может быть сочетанием любого из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1a6e9-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="1a6e9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1a6e9-111">Value</span></span>                                                              | <span data-ttu-id="1a6e9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1a6e9-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1a6e9-113">**const без знака Short** **\_ ненулевое значение = 0;**</span><span class="sxs-lookup"><span data-stu-id="1a6e9-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="1a6e9-114">Клиент не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="1a6e9-115">**const неподписанных коротких** **активных активаций \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="1a6e9-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="1a6e9-116">Клиент является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="1a6e9-117">**const неподписанного короткого** **ключа \_ инпутактиве = 2;**</span><span class="sxs-lookup"><span data-stu-id="1a6e9-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="1a6e9-118">Клиент имеет входные данные (активный клиент верхнего символа).</span><span class="sxs-lookup"><span data-stu-id="1a6e9-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="1a6e9-119">Если несколько клиентских приложений совместно используют один и тот же символ, то активный клиент символа получает ввод с помощью мыши (например, элемент управления агента Microsoft Agent щелкнул или перетаскивает события).</span><span class="sxs-lookup"><span data-stu-id="1a6e9-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="1a6e9-120">Аналогично, когда отображается несколько символов, активный клиент самого верхнего символа (также известный как клиент ввода) получает события [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6e9-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="1a6e9-121">При изменении активного клиента символа это событие возвращает идентификатор этого символа и **значение true** , если приложение становится активным клиентом символа, или **значение false** , если оно больше не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="1a6e9-122">Клиентское приложение может получить это событие, когда пользователь выбирает запись другого клиентского приложения во всплывающем меню символа или с помощью команды Voice, клиентское приложение изменяет свое активное состояние, или другое клиентское приложение завершает свое подключение к Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="1a6e9-123">Агент отправляет это событие только в клиентские приложения, которые напрямую затронуты, — на те, которые либо становятся активными клиентами, либо останавливаются активным клиентом.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="1a6e9-124">Вы можете использовать метод [**Activate**](iagentcharacter--activate.md) , чтобы задать, является ли приложение активным клиентом символа, или сделать так, чтобы ваше приложение было клиентом input-Active (что также делает символ самым верхним).</span><span class="sxs-lookup"><span data-stu-id="1a6e9-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a6e9-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="1a6e9-125">See Also</span></span>

<span data-ttu-id="1a6e9-126">[**Иажентчарактер:: Activate**](iagentcharacter--activate.md), [**иажентчарактерекс:: onactive**](iagentcharacterex--getactive.md), [**иажентнотифисинк:: активатеинпутстате**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="1a6e9-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





