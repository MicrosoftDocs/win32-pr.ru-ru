---
description: В этом разделе показано, как сгруппировать XAudio2 методы, чтобы они вступили в силу одновременно.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Руководство: группировка звуковых методов как набора операций'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911103"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="7fb96-103">Руководство: группировка звуковых методов как набора операций</span><span class="sxs-lookup"><span data-stu-id="7fb96-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="7fb96-104">В этом разделе показано, как сгруппировать XAudio2 методы, чтобы они вступили в силу одновременно.</span><span class="sxs-lookup"><span data-stu-id="7fb96-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="7fb96-105">Группировка звуковых методов в виде набора операций</span><span class="sxs-lookup"><span data-stu-id="7fb96-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="7fb96-106">Объявите счетчик глобального набора операций.</span><span class="sxs-lookup"><span data-stu-id="7fb96-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="7fb96-107">Счетчик [набора операций](operation-sets.md) гарантирует уникальность каждого набора операций.</span><span class="sxs-lookup"><span data-stu-id="7fb96-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="7fb96-108">Увеличьте значение глобального счетчика.</span><span class="sxs-lookup"><span data-stu-id="7fb96-108">Increment the global counter.</span></span>

    <span data-ttu-id="7fb96-109">Каждый раз при отправке нового [набора операций](operation-sets.md)глобальный счетчик должен увеличиваться, чтобы гарантировать уникальность каждого набора.</span><span class="sxs-lookup"><span data-stu-id="7fb96-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="7fb96-110">Сгруппируйте вызовы методов, задав параметры их [набора операций](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="7fb96-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="7fb96-111">Задайте для параметров [набора операций](operation-sets.md) текущее значение глобального счетчика.</span><span class="sxs-lookup"><span data-stu-id="7fb96-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="7fb96-112">В этом случае четыре вызова [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) группируются как один [набор операций](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="7fb96-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="7fb96-113">Группирование вызовов приводит к тому, что все четыре звуковых сигнала запускаются в точно такое же время.</span><span class="sxs-lookup"><span data-stu-id="7fb96-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="7fb96-114">Запуск [набора операций](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="7fb96-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="7fb96-115">После вызова всех методов в наборе запустите набор, вызвав [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) с текущим значением глобального счетчика.</span><span class="sxs-lookup"><span data-stu-id="7fb96-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7fb96-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7fb96-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb96-117">Наборы операций</span><span class="sxs-lookup"><span data-stu-id="7fb96-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="7fb96-118">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="7fb96-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7fb96-119">Наборы операций XAudio2</span><span class="sxs-lookup"><span data-stu-id="7fb96-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
