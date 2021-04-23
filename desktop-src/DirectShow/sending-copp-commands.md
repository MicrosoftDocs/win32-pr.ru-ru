---
description: Отправка команд Копп
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Отправка команд Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672995"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="ddd55-103">Отправка команд Копп</span><span class="sxs-lookup"><span data-stu-id="ddd55-103">Sending COPP Commands</span></span>

<span data-ttu-id="ddd55-104">Чтобы отправить команду на сертификат сертифицированной защиты выхода (Копп), заполните структуру [**амкоппкомманд**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ddd55-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="ddd55-105">**гуидкоммандид**.</span><span class="sxs-lookup"><span data-stu-id="ddd55-105">**guidCommandID**.</span></span> <span data-ttu-id="ddd55-106">Идентификатор GUID, определяющий команду.</span><span class="sxs-lookup"><span data-stu-id="ddd55-106">The GUID that identifies the command.</span></span> <span data-ttu-id="ddd55-107">См. Справочник по командам Копп.</span><span class="sxs-lookup"><span data-stu-id="ddd55-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="ddd55-108">**двсекуенце**.</span><span class="sxs-lookup"><span data-stu-id="ddd55-108">**dwSequence**.</span></span> <span data-ttu-id="ddd55-109">Порядковый номер команды.</span><span class="sxs-lookup"><span data-stu-id="ddd55-109">The command sequence number.</span></span> <span data-ttu-id="ddd55-110">Увеличьте это значение после каждой команды.</span><span class="sxs-lookup"><span data-stu-id="ddd55-110">Increment this value after each command.</span></span> <span data-ttu-id="ddd55-111">(Это значение отображается как **укоммандсек** при [инициации сеанса Копп](initiating-a-copp-session.md).)</span><span class="sxs-lookup"><span data-stu-id="ddd55-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="ddd55-112">**кбсизедата**.</span><span class="sxs-lookup"><span data-stu-id="ddd55-112">**cbSizeData**.</span></span> <span data-ttu-id="ddd55-113">Размер данных в байтах, необходимых для выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="ddd55-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="ddd55-114">**Комманддата**.</span><span class="sxs-lookup"><span data-stu-id="ddd55-114">**CommandData**.</span></span> <span data-ttu-id="ddd55-115">Данные для команды.</span><span class="sxs-lookup"><span data-stu-id="ddd55-115">Data for the command.</span></span>

<span data-ttu-id="ddd55-116">После заполнения этих данных Вычислите MAC для команды:</span><span class="sxs-lookup"><span data-stu-id="ddd55-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="ddd55-117">Вычислите тег ОМАК-1 для блока данных, который отображается после элемента **маккди** структуры **амкоппкомманд** .</span><span class="sxs-lookup"><span data-stu-id="ddd55-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="ddd55-118">Скопируйте это значение в элемент **маккди** структуры.</span><span class="sxs-lookup"><span data-stu-id="ddd55-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="ddd55-119">Теперь передайте структуру методу [**иамцертифиедаутпутпротектион::P ротектионкомманд**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .</span><span class="sxs-lookup"><span data-stu-id="ddd55-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddd55-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ddd55-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd55-121">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="ddd55-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



