---
title: Правила для нескольких каналов
description: Правила для нескольких каналов в одном вызове в удаленном вызове процедур (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488105"
---
# <a name="rules-for-multiple-pipes"></a><span data-ttu-id="a4541-103">Правила для нескольких каналов</span><span class="sxs-lookup"><span data-stu-id="a4541-103">Rules for Multiple Pipes</span></span>

<span data-ttu-id="a4541-104">В \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] любом сочетании в одном вызове можно сочетать параметры вертикального канала, out и in, но необходимо обработать каналы в определенном порядке, как показано в следующем примере псевдокода:</span><span class="sxs-lookup"><span data-stu-id="a4541-104">You can combine \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], and \[**in, out**\] pipe parameters in any combination in a single call, but you must process the pipes in a specific order, as shown in the following pseudocode example:</span></span>

> [!Note]  
> <span data-ttu-id="a4541-105">Эта функция больше не поддерживается в Windows Vista и более поздних платформах.</span><span class="sxs-lookup"><span data-stu-id="a4541-105">This feature is no longer supported in Windows Vista and later platforms.</span></span>

 

-   <span data-ttu-id="a4541-106">Получите данные из каждого входного канала, начиная с первого (крайнего левого) \[ **в** \] параметре, и продолжая по порядку выполнять сток каждого канала перед началом обработки следующего.</span><span class="sxs-lookup"><span data-stu-id="a4541-106">Get the data from every input pipe, starting with the first (leftmost) \[**in**\] parameter, and continuing in order, draining each pipe before beginning to process the next.</span></span>
-   <span data-ttu-id="a4541-107">После полной обработки каждого входного канала отправьте данные для выходных каналов, снова начиная с первого \[ **выходного** \] параметра и продолжая по порядку, заполняя каждый канал перед началом обработки следующего.</span><span class="sxs-lookup"><span data-stu-id="a4541-107">After every input pipe has been completely processed, send the data for the output pipes, again starting with the first \[**out**\] parameter, and continuing in order, filling each pipe before beginning to process the next.</span></span>

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 