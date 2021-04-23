---
title: Метод Listen
description: Метод Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069875"
---
# <a name="listen-method"></a><span data-ttu-id="0a0e7-103">Метод Listen</span><span class="sxs-lookup"><span data-stu-id="0a0e7-103">Listen Method</span></span>

<span data-ttu-id="0a0e7-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a0e7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0a0e7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="0a0e7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a0e7-106">Включает режим прослушивания (распознавание речи) в течение времени.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="0a0e7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0a0e7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0a0e7-108">\*агент. ***Символы \* \* \* \* ("*** чарактерид \* \* *"). Состояние прослушивания* \*  </span><span class="sxs-lookup"><span data-stu-id="0a0e7-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="0a0e7-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="0a0e7-109">Part</span></span>    | <span data-ttu-id="0a0e7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0a0e7-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0e7-111">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="0a0e7-111">*State*</span></span> | <span data-ttu-id="0a0e7-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-112">Required.</span></span> <span data-ttu-id="0a0e7-113">Логическое значение, определяющее, следует ли включать или отключать режим прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="0a0e7-114">**Значение true** Включает режим прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="0a0e7-115">**Значение false** Выключает режим прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a0e7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a0e7-116">Remarks</span></span>

<span data-ttu-id="0a0e7-117">Присвоение этому методу значения **true** включает режим прослушивания (включает распознавание речи) в течение фиксированного периода времени (10 секунд).</span><span class="sxs-lookup"><span data-stu-id="0a0e7-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="0a0e7-118">Пока нельзя задать значение времени ожидания, можно отключить режим прослушивания до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="0a0e7-119">Если вы (или другой клиент) успешно установили режим прослушивания в и вы пытаетесь установить это свойство в **значение true** до истечения времени ожидания, метод завершается успешно и сбрасывает время ожидания. Однако если режим прослушивания включен, так как пользователь нажимает клавишу прослушивания, метод завершается, но время ожидания игнорируется, а режим прослушивания завершается в зависимости от взаимодействия пользователя с ключом прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="0a0e7-120">Этот метод выполняется успешно только при вызове из input-Active Client и при запуске речевых служб.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="0a0e7-121">Чтобы убедиться, что службы речи запущены, запросите или задайте [**срмодеид**](srmodeid-property.md) или настройте [**голосовую**](voice-property.md) настройку для [**команды**](/windows/desktop/lwef/the-command-object) перед вызовом **Listen** . в противном случае произойдет сбой метода.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="0a0e7-122">Чтобы определить успешность этого метода, вызовите его как функцию и возвратит логическое значение, указывающее, успешно ли выполнен метод.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="0a0e7-123">Метод также завершается ошибкой, если пользователь нажимает клавишу прослушивания, и вы пытаетесь установить значение **Listen** **false**.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="0a0e7-124">Однако, если пользователь выпустил ключ прослушивания, а режим прослушивания не истек, он завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="0a0e7-125">**Прослушивание** также завершается ошибкой, если отсутствует совместимый механизм распознавания речи, соответствующий параметру [**LanguageID**](languageid-property.md) символа, пользователь отключил речевой ввод с помощью вкладки свойств Microsoft Agent или звуковое устройство занято.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="0a0e7-126">Если для этого метода задано **значение true**, сервер запускает событие [**листенстарт**](listenstart-event.md) .</span><span class="sxs-lookup"><span data-stu-id="0a0e7-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="0a0e7-127">Сервер отправляет [**листенкомплете**](listencomplete-event.md) при завершении времени ожидания режима прослушивания или при установке параметра **Listen** в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="0a0e7-128">Этот метод не вызывает автоматический вызов метода [**останавливает**](stop-method.md) и воспроизводит анимацию состояния прослушивания, так как сервер выполняет нажатие клавиши прослушивания.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="0a0e7-129">Это позволяет определить, следует ли прерывать текущую анимацию с помощью анимации [**листенстарт**](listenstart-event.md) , вызвав метод **остановить** и воспроизводить собственную анимацию.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="0a0e7-130">Однако при обнаружении пользователем utterance вызывается метод " **останавливает** " и воспроизводит анимацию состояния слуха.</span><span class="sxs-lookup"><span data-stu-id="0a0e7-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a0e7-131">См. также:</span><span class="sxs-lookup"><span data-stu-id="0a0e7-131">See Also</span></span>

<span data-ttu-id="0a0e7-132">[**Свойство LanguageID**](languageid-property.md), [**событие листенкомплете**](listencomplete-event.md), [**событие листенстарт**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="0a0e7-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

