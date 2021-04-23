---
title: Иажентчарактер Стопалл
description: Иажентчарактер Стопалл
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710113"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="018a6-103">Иажентчарактер:: Стопалл</span><span class="sxs-lookup"><span data-stu-id="018a6-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="018a6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="018a6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="018a6-105">Останавливает все анимации (запросы) и удаляет их из очереди анимации символа.</span><span class="sxs-lookup"><span data-stu-id="018a6-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="018a6-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*лтипе*</span><span class="sxs-lookup"><span data-stu-id="018a6-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="018a6-107">Битовое поле, указывающее типы запросов, которые нужно приостанавливаться (и которые удаляются из очереди символов), состоящие из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="018a6-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="018a6-108">Тип **беззнаковой неподписанного типа Long без знака** **\_ \_ ALL = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="018a6-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="018a6-109">Останавливает все запросы анимации, включая запросы на [**подготовку**](iagentcharacter--prepare.md) , не связанные с очередями.</span><span class="sxs-lookup"><span data-stu-id="018a6-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="018a6-110">Тип **постоянного неподписанного длинного** **\_ типа " \_ воспроизвести = 0x00000001;** "</span><span class="sxs-lookup"><span data-stu-id="018a6-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="018a6-111">Останавливает все запросы на воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="018a6-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="018a6-112">**неподписанный длинный** **тип останавливаемого типа беззнакового \_ \_ перемещения = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="018a6-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="018a6-113">Останавливает все запросы на [**Перемещение**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="018a6-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="018a6-114">Тип **неподписанного длинного типа Long без знака** **\_ \_ : выговаривать = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="018a6-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="018a6-115">Останавливает все запросы на [**Распознавание речи**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="018a6-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="018a6-116">**неподписанный длинный тип беззнакового** **\_ типа завершения \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="018a6-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="018a6-117">Останавливает все отложенные запросы на [**подготовку**](iagentcharacter--prepare.md) .</span><span class="sxs-lookup"><span data-stu-id="018a6-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="018a6-118">Тип **однобайтового типа const беззнаковых** **\_ типов \_ нонкуеуедпрепаре = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="018a6-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="018a6-119">Останавливает все запросы на [**подготовку**](iagentcharacter--prepare.md) , не относящиеся к очереди.</span><span class="sxs-lookup"><span data-stu-id="018a6-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="018a6-120">Невидимый тип **беззнакового неподписанного** **\_ типа long \_ = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="018a6-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="018a6-121">Останавливает все запросы на [**Скрытие**](iagentcharacter--hide.md) или [**Отображение**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="018a6-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="018a6-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="018a6-122">See Also</span></span>

[<span data-ttu-id="018a6-123">**Иажентчарактер:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="018a6-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





