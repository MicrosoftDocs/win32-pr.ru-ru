---
title: Прерывание Иажентчарактер
description: Прерывание Иажентчарактер
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987373"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="2a065-103">Иажентчарактер:: interrupt</span><span class="sxs-lookup"><span data-stu-id="2a065-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="2a065-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a065-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="2a065-105">Прерывает указанную анимацию (запрос) другого символа.</span><span class="sxs-lookup"><span data-stu-id="2a065-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="2a065-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2a065-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="2a065-107">Когда функция возвращает значение, *пдврекид* содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="2a065-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="2a065-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*дврекид*</span><span class="sxs-lookup"><span data-stu-id="2a065-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="2a065-109">Идентификатор запроса для прерывания.</span><span class="sxs-lookup"><span data-stu-id="2a065-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="2a065-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="2a065-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="2a065-111">Адрес переменной, которая получает идентификатор запроса на **прерывание** .</span><span class="sxs-lookup"><span data-stu-id="2a065-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="2a065-112">При загрузке нескольких символов можно использовать этот метод для синхронизации анимации между символами.</span><span class="sxs-lookup"><span data-stu-id="2a065-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="2a065-113">Например, если другой символ находится в циклической анимации, этот метод останавливает циклическую анимацию и запускает следующую анимацию в очереди символов.</span><span class="sxs-lookup"><span data-stu-id="2a065-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="2a065-114">**Прерывание** останавливает существующую анимацию, но не очищает очередь анимации символа.</span><span class="sxs-lookup"><span data-stu-id="2a065-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="2a065-115">Он запускает следующую анимацию в очереди символов.</span><span class="sxs-lookup"><span data-stu-id="2a065-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="2a065-116">Чтобы остановить и очистить очередь символов, используйте метод [**остановки**](/windows/desktop/lwef/iagentcharacter--stop) .</span><span class="sxs-lookup"><span data-stu-id="2a065-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="2a065-117">Этот метод нельзя использовать для самостоятельного прерывания символа, поскольку сервер Microsoft Agent помещает метод **прерывания** в очередь анимации символа.</span><span class="sxs-lookup"><span data-stu-id="2a065-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="2a065-118">Таким образом, **прерывание** можно использовать только для остановки анимации другого символа, который вы загрузили.</span><span class="sxs-lookup"><span data-stu-id="2a065-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 