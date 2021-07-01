---
title: Иажентчарактер Стопалл
description: Иажентчарактер Стопалл
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120917"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="3dff6-103">Иажентчарактер:: Стопалл</span><span class="sxs-lookup"><span data-stu-id="3dff6-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="3dff6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3dff6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="3dff6-105">Останавливает все анимации (запросы) и удаляет их из очереди анимации символа.</span><span class="sxs-lookup"><span data-stu-id="3dff6-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="3dff6-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*лтипе*</span><span class="sxs-lookup"><span data-stu-id="3dff6-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="3dff6-107">Битовое поле, указывающее типы запросов, которые нужно приостанавливаться (и которые удаляются из очереди символов), состоящие из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3dff6-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



| <span data-ttu-id="3dff6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3dff6-108">Value</span></span>                                                                                  |  <span data-ttu-id="3dff6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3dff6-109">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dff6-110">Тип **беззнаковой неподписанного типа Long без знака** **\_ \_ ALL = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-110">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="3dff6-111">Останавливает все запросы анимации, включая запросы на [**подготовку**](iagentcharacter--prepare.md) , не связанные с очередями.</span><span class="sxs-lookup"><span data-stu-id="3dff6-111">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="3dff6-112">Тип **постоянного неподписанного длинного** **\_ типа " \_ воспроизвести = 0x00000001;** "</span><span class="sxs-lookup"><span data-stu-id="3dff6-112">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="3dff6-113">Останавливает все запросы на воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="3dff6-113">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="3dff6-114">**неподписанный длинный** **тип останавливаемого типа беззнакового \_ \_ перемещения = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-114">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="3dff6-115">Останавливает все запросы на [**Перемещение**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="3dff6-115">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="3dff6-116">Тип **неподписанного длинного типа Long без знака** **\_ \_ : выговаривать = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-116">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="3dff6-117">Останавливает все запросы на [**Распознавание речи**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff6-117">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="3dff6-118">**неподписанный длинный тип беззнакового** **\_ типа завершения \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-118">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="3dff6-119">Останавливает все отложенные запросы на [**подготовку**](iagentcharacter--prepare.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff6-119">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="3dff6-120">Тип **однобайтового типа const беззнаковых** **\_ типов \_ нонкуеуедпрепаре = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-120">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="3dff6-121">Останавливает все запросы на [**подготовку**](iagentcharacter--prepare.md) , не относящиеся к очереди.</span><span class="sxs-lookup"><span data-stu-id="3dff6-121">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="3dff6-122">Невидимый тип **беззнакового неподписанного** **\_ типа long \_ = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="3dff6-122">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="3dff6-123">Останавливает все запросы на [**Скрытие**](iagentcharacter--hide.md) или [**Отображение**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff6-123">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3dff6-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3dff6-124">See Also</span></span>

[<span data-ttu-id="3dff6-125">**Иажентчарактер:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="3dff6-125">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





