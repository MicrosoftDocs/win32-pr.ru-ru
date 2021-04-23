---
title: Иажентчарактерекс прослушивание
description: Иажентчарактерекс прослушивание
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330696"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="35ac4-103">Иажентчарактерекс:: Listen</span><span class="sxs-lookup"><span data-stu-id="35ac4-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="35ac4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35ac4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="35ac4-105">Включает или выключает режим прослушивания (вход распознавания речи).</span><span class="sxs-lookup"><span data-stu-id="35ac4-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="35ac4-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35ac4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="35ac4-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*блистен*</span><span class="sxs-lookup"><span data-stu-id="35ac4-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="35ac4-108">Флаг режима прослушивания.</span><span class="sxs-lookup"><span data-stu-id="35ac4-108">Listening mode flag.</span></span> <span data-ttu-id="35ac4-109">Если этот параметр имеет **значение true**, режим прослушивания включен; Если задано **значение false**, режим прослушивания отключен.</span><span class="sxs-lookup"><span data-stu-id="35ac4-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="35ac4-110">Установка этого метода в **значение true** включает режим прослушивания (включает распознавание речи) в течение фиксированного периода времени.</span><span class="sxs-lookup"><span data-stu-id="35ac4-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="35ac4-111">Пока нельзя задать значение времени ожидания, можно отключить режим прослушивания до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="35ac4-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="35ac4-112">Кроме того, если режим прослушивания уже включен, так как вы (или другой клиент) успешно установили для метода **значение true** до истечения времени ожидания, метод выполняется успешно и сбрасывает время ожидания. Однако если режим прослушивания уже включен, так как пользователь нажимает клавишу прослушивания, метод завершается, но время ожидания игнорируется, а режим прослушивания завершается в зависимости от взаимодействия пользователя с ключом прослушивания.</span><span class="sxs-lookup"><span data-stu-id="35ac4-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="35ac4-113">Этот метод будет выполнен только при вызове клиентом ввода-активного.</span><span class="sxs-lookup"><span data-stu-id="35ac4-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="35ac4-114">Поэтому метод завершится ошибкой, если клиент не является активным клиентом самого верхнего символа.</span><span class="sxs-lookup"><span data-stu-id="35ac4-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="35ac4-115">Метод также завершится ошибкой, если вы попытаетесь установить для метода **значение false** и пользователь нажимает клавишу прослушивания.</span><span class="sxs-lookup"><span data-stu-id="35ac4-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="35ac4-116">Также может произойти сбой, если отсутствует совместимый механизм распознавания речи, соответствующий параметру идентификатора языка символа, или пользователь отключил речевой ввод с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="35ac4-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="35ac4-117">Однако метод не будет работать, если звуковое устройство занято.</span><span class="sxs-lookup"><span data-stu-id="35ac4-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="35ac4-118">Если для этого метода задано **значение true**, сервер запускает событие [**Иажентнотифисинкекс:: листенингстате**](iagentnotifysinkex--listeningstate.md) .</span><span class="sxs-lookup"><span data-stu-id="35ac4-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="35ac4-119">Сервер также отправляет **иажентнотифисинкекс:: листенингстате** по завершении времени ожидания в режиме ожидания или при установке [**Иажентчарактерекс:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) **false**.</span><span class="sxs-lookup"><span data-stu-id="35ac4-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="35ac4-120">Этот метод не вызывает автоматически [**иажентчарактер:: стопалл**](iagentcharacter--stopall.md) и воспроизводит анимацию состояния прослушивания символа, как происходит, когда пользователь нажимает клавишу прослушивания.</span><span class="sxs-lookup"><span data-stu-id="35ac4-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="35ac4-121">Это позволяет использовать событие [**иажентнотифисинкекс:: листенингстате**](iagentnotifysinkex--listeningstate.md) , чтобы определить, следует ли прерывать текущую анимацию и воспроизводить соответствующую анимацию.</span><span class="sxs-lookup"><span data-stu-id="35ac4-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="35ac4-122">Однако после обнаружения пользователя utterance сервер автоматически вызывает **иажентчарактер:: стопалл** и воспроизводит анимацию состояния слуха.</span><span class="sxs-lookup"><span data-stu-id="35ac4-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="35ac4-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="35ac4-123">See Also</span></span>

<span data-ttu-id="35ac4-124">[**Иажентнотифисинкекс:: листенингстате**](iagentnotifysinkex--listeningstate.md), [ **иажентспичинпутпропертиес:: enable**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="35ac4-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




